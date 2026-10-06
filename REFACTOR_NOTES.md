# Customer Service Performance — UI Refactor

## What changed

- Added Arabic as the default UI language.
- Added Arabic/English language switcher with localStorage persistence.
- Added real RTL support at the document and layout level.
- Added Cairo font support for Arabic.
- Added a centralized i18n layer at `src/lib/i18n.tsx`.
- Added reusable `LanguageSwitcher` component.
- Updated date formatting to follow the active language.
- Added Ctrl/Cmd + K shortcut to focus employee search.
- Improved mobile RTL sidebar positioning and navigation behavior.
- Kept the existing API, scoring logic, database schema, Excel import, Excel/PDF export, reports, evaluations, rankings, and KPI settings intact.

## Architecture direction

The existing feature logic remains compatible, while cross-cutting UI concerns are moved into reusable modules. The next recommended step is to split `src/App.tsx` into route-level modules (`pages/overview`, `pages/employees`, `pages/evaluations`, `pages/rankings`, `pages/reports`, `pages/settings`) without changing API contracts.

## Validation

TypeScript parsing was checked successfully. A full typecheck/build requires the project's workspace dependencies (`node`, `vite/client` type packages, etc.) to be installed with the repository's normal pnpm workflow.
