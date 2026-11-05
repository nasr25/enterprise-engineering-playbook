# 9. Mobile Application Lifecycle and State Management

Rules `MOB-181`–`MOB-200`. These requirements extend `MOB-013`–`MOB-017`, `MOB-075`, `MOB-100`, `MOB-162`, and `MOB-167`. They apply to Flutter and equivalent native/cross-platform lifecycle mechanisms.

## Mandatory Requirements

- **MOB-181 — Lifecycle ownership:** Every non-trivial mobile app MUST designate one lifecycle coordinator (or equivalent bounded ownership) for foreground/background state, session revalidation, polling, sockets, synchronization and sensitive-screen protection; avoid per-screen duplicate global listeners.
- **MOB-182 — State coverage:** Critical flows MUST explicitly account for active/resumed, inactive/interrupted, hidden/not visible, paused/background, process death/termination, and restoration. State names and event order vary by framework/OS.
- **MOB-183 — No guaranteed callbacks:** Correctness MUST NOT depend on receiving a final pause, detach, dispose or termination callback. Persist critical state at durable business checkpoints and recover from abrupt process death.
- **MOB-184 — Resume revalidation:** On foreground return, revalidate authentication/session expiry, authorization-sensitive data and freshness according to risk; avoid unconditional full reloads or repeated login prompts.
- **MOB-185 — Sensitive content protection:** On backgrounding or loss of visibility, protect sensitive app-switcher snapshots where supported, pause sensitive media/camera previews as appropriate, and prevent leakage through notifications, logs or screenshots to the extent platform controls permit.
- **MOB-186 — Resource coordination:** Suspend or reduce unnecessary polling, animations, location/camera/microphone work, subscriptions and sockets when not needed; resume only owned resources, without leaking listeners or duplicating connections.
- **MOB-187 — Duplicate-request prevention:** Foreground restoration MUST coalesce/deduplicate equivalent in-flight reads, cancel stale requests where appropriate and prevent overlapping refresh/sync loops. Mutations MUST retain server-side idempotency and authorization.
- **MOB-188 — Network and sync transitions:** Handle connectivity changes independently of lifecycle callbacks; retries MUST be bounded, backoff-aware and safe against duplicate business effects. Network availability does not prove backend reachability.
- **MOB-189 — Background execution constraints:** Background work MUST use approved OS mechanisms and declared capabilities; execution time, frequency and completion are not guaranteed. Design for cancellation, expiry and later recovery.
- **MOB-190 — Durable state and restoration:** Persist only necessary non-sensitive state; use protected storage for sensitive values, explicit schema/version migration, and deterministic restoration after OS process recreation.
- **MOB-191 — Foreground session concurrency:** Refresh tokens MUST be single-flight or otherwise coordinated; concurrent resume, API calls and push/deep-link entry MUST NOT race to overwrite credentials or resurrect a logged-out session.
- **MOB-192 — Navigation and external entry:** Deep links, notification taps, authentication callbacks and pending routes MUST be validated and reconciled after lifecycle restoration; never bypass server-side access checks.
- **MOB-193 — Lifecycle-aware UX:** Loading, offline, expired-session, conflict and interrupted-operation states MUST be explicit; do not show success for a backgrounded action until the authoritative outcome is confirmed.
- **MOB-194 — Power and data efficiency:** Background polling, high-frequency timers and location updates MUST have documented business justification, bounded frequency and battery/data impact measurements where material.
- **MOB-195 — Platform differences:** iOS and Android implementations MUST be reviewed separately for lifecycle transitions, background restrictions, app-switcher behavior, permissions and OS-initiated process death.
- **MOB-196 — Flutter observation:** Flutter applications SHOULD use `AppLifecycleListener` or `WidgetsBindingObserver.didChangeAppLifecycleState` with clear registration/removal ownership; callbacks MUST remain lightweight and non-blocking.
- **MOB-197 — Flutter state mapping:** Flutter's `AppLifecycleState` values `resumed`, `inactive`, `hidden`, `paused`, and `detached` MUST be interpreted per platform; `hidden` can be synthesized, and `paused` is not a universal cross-platform event. Do not equate `detached` with guaranteed process termination.
- **MOB-198 — Flutter cleanup:** Dispose/cancel `StreamSubscription`, `Timer`, `AnimationController`, `TextEditingController`, `FocusNode`, `AppLifecycleListener`, and other owned resources at the appropriate component/service lifetime; pausing is not equivalent to disposal.
- **MOB-199 — Lifecycle test matrix:** Automated and device tests MUST cover resume after short/long background, inactive interruptions (calls/permission prompts), network loss/recovery, process kill and relaunch, expired/rotated token, duplicate resume events, concurrent refreshes, deep-link/push entry and interrupted writes for critical flows.
- **MOB-200 — Evidence and monitoring:** Critical lifecycle failures (duplicate requests, lost sync, stale auth, background crashes, excessive battery use) MUST have measurable diagnostics and review evidence without collecting secrets or unnecessary personal data.

## Flutter Lifecycle Decision Matrix

| Flutter state / event | Expected engineering response | Important caveat |
|---|---|---|
| `resumed` / `onResume` | Reconcile session and freshness; restart required polling/sockets once; reconcile pending sync | May fire repeatedly; deduplicate and throttle refresh |
| `inactive` / `onInactive` | Protect transient sensitive UI and pause focus-sensitive interaction as needed | Not synonymous with background; can be a short interruption |
| `hidden` / `onHide` | Mark UI not visible, protect sensitive surfaces and prepare to suspend unnecessary work | Framework may synthesize this transition |
| `paused` / `onPause` | Stop nonessential foreground work; preserve recoverable state; use OS-approved background tasks only | Not guaranteed before process death; platform-dependent |
| `detached` / `onDetach` | Release resources when possible, tolerate loss of view attachment | Not a reliable last-chance persistence hook |
| Process killed / cold launch | Restore from durable state, revalidate session and reconcile pending operations | No callback is guaranteed at kill time |

Do not implement business mutations merely because a lifecycle callback fired. Keep lifecycle callbacks lightweight; schedule expensive work through owned, cancellable services.

## Flutter Implementation Pattern (Illustrative)

```dart
class LifecycleCoordinator {
  LifecycleCoordinator(this.session, this.refresh, this.polling);

  final SessionService session;
  final RefreshService refresh;
  final PollingService polling;
  AppLifecycleListener? _listener;
  Future<void>? _resumeInFlight;

  void start() {
    _listener ??= AppLifecycleListener(
      onResume: () => _resumeOnce(),
      onPause: polling.stop,
      onHide: polling.stop,
    );
  }

  void _resumeOnce() {
    _resumeInFlight ??= _reconcile().whenComplete(() {
      _resumeInFlight = null;
    });
  }

  Future<void> _reconcile() async {
    await session.revalidateIfNeeded();
    await refresh.refreshStaleData();
    polling.startIfAllowed();
  }

  void dispose() {
    _listener?.dispose();
    _listener = null;
    polling.stop();
  }
}
```

This is pseudocode illustrating lifecycle ownership and single-flight resume behavior, not a complete production implementation. In real code, guard against disposal during asynchronous resume, handle failures, use platform-specific behavior, and keep authentication/authorization server-authoritative.

## Required Review Evidence

- Lifecycle state-transition diagram and ownership map
- Background-task capability/permission and battery impact review
- Session refresh, polling/socket, cache and sync state-machine tests
- iOS and Android test matrix including abrupt termination and restoration
- Traces or test evidence proving no duplicate API calls on resume
- Sensitive snapshot and notification privacy verification
- Documented exceptions and platform-specific limitations
