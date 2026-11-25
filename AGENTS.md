# Project Development Standards

These instructions apply to every change in this repository.

## Required workflow
Follow PLAN → DESIGN → DEVELOP → INTEGRATE → TEST → DELIVERY GATE.

1. Inspect the existing code, dependencies, and behavior before editing.
2. Identify the smallest safe change. Preserve working features and existing data formats.
3. Define the UI intent and interaction states before implementation.
4. Implement modular, readable, maintainable code. Avoid unnecessary dependencies and duplicated logic.
5. Integrate changes with existing flows and storage.
6. Run relevant checks. Never claim a test passed unless it was actually run.
7. Complete the evidence-based Delivery Gate before reporting completion.

## UI/UX standards
Apply Anti-Slop DURING, Impeccable, and UI UX Pro Max principles throughout planning and implementation:
- Design with a clear purpose and a distinctive visual direction. Avoid generic template-like layouts and decorative elements without function.
- Maintain consistent design tokens for color, typography, spacing, borders, radii, shadows, and interaction states.
- Establish clear hierarchy, readable content, and predictable navigation.
- Support desktop, tablet, and mobile layouts.
- Provide visible focus states, semantic HTML, accessible labels, keyboard operation, and adequate touch targets.
- Respect prefers-reduced-motion.
- Include useful loading, empty, error, success, and disabled states where relevant.
- Every visible button, link, form, filter, and navigation item must perform its stated action. Remove or clearly disable controls that have no behavior.

## Engineering and security
- Keep code simple, modular, and consistent with the current project architecture.
- Validate and normalize user input at the appropriate boundary.
- Render user-provided text safely. Do not inject untrusted values as HTML.
- Do not commit secrets, API keys, credentials, or private tokens.
- Handle storage and network failures without silently losing user data.
- Preserve backward compatibility unless a migration is explicitly planned.
- Use dependencies only when they provide clear value. Document external runtime dependencies.

## FinancePro project constraints
- Preserve the existing financeProData LocalStorage key and compatible transaction fields unless a deliberate migration is implemented.
- Explain that LocalStorage data belongs to the current browser/device. Do not imply cloud synchronization.
- Keep charts and Excel export resilient when their CDN libraries fail to load.
- Do not add backend services or authentication unless the requested scope requires them.

## Delivery Gate
Report PASS or FAIL with evidence for:
- Existing feature preservation and data compatibility.
- Functional controls and form validation.
- Responsive layout at relevant breakpoints.
- Accessibility basics, including labels, focus, keyboard use, and reduced motion.
- Error, empty, and success states.
- JavaScript syntax, build, lint, or other available automated checks.
- Security and secret handling.

Clearly separate checks actually executed from manual checks still required. Do not claim browser/device testing without performing it. List known limitations and deployment implications.