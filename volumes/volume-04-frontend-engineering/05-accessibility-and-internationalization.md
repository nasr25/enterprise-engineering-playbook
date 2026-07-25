# Accessibility and Internationalization

## Purpose

Ensure digital services are usable by people with diverse abilities, devices, languages, and reading directions.

## Mandatory Rules

- **FE-061** — User interfaces must meet the organization’s approved accessibility target and applicable legal or policy obligations.
- **FE-062** — Semantic HTML and native controls must be preferred over custom equivalents.
- **FE-063** — All interactive elements must be operable by keyboard with visible focus.
- **FE-064** — Focus order and focus restoration must follow user intent during routing, dialogs, errors, and dynamic updates.
- **FE-065** — Form fields must have programmatic labels, instructions, validation association, and accessible error summaries.
- **FE-066** — Color must not be the only means of conveying status or meaning.
- **FE-067** — Text and essential graphical elements must maintain approved contrast levels.
- **FE-068** — Images must provide meaningful alternatives or be marked decorative.
- **FE-069** — Dynamic status changes must be exposed appropriately to assistive technologies without excessive announcements.
- **FE-070** — Automated accessibility checks must run in CI, supplemented by keyboard and assistive-technology testing for critical journeys.
- **FE-071** — User-visible text must be externalized from components when localization is required.
- **FE-072** — Layouts must support text expansion and must not rely on fixed string lengths.
- **FE-073** — Dates, times, numbers, currencies, pluralization, and sorting must use locale-aware behavior.
- **FE-074** — Right-to-left layouts must be tested as a complete interaction model, not only mirrored visually.
- **FE-075** — Language fallback, missing translations, and mixed-language content behavior must be defined.

## Required Evidence

- Accessibility test report
- Keyboard journey results
- Screen-reader checks for critical workflows
- RTL and localization screenshots
- Translation ownership and release process