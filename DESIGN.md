# FinancePro Design System

## Product identity
FinancePro is a personal finance workspace for recording income and expenses, understanding cash flow, and reviewing a reliable transaction history.

## Visual direction: grounded clarity
The interface uses an editorial, nature-inspired visual language. Deep evergreen communicates stability. Soft mineral green and warm off-white create a calm working surface. A restrained lime accent highlights the brand and active navigation. Income and expense colors remain semantic.

### Core tokens
| Token | Value | Purpose |
|---|---|---|
| Evergreen | `#12372F` | Brand structure, sidebar, balance panel |
| Forest | `#1D594B` | Primary action and active state |
| Leaf | `#C9EF75` | Brand mark and restrained accent |
| Canvas | `#F3F4EE` | Main page background |
| Surface | `#FFFEFA` | Cards, forms, and tables |
| Ink | `#1C302B` | Primary text |
| Muted | `#60716A` | Supporting text |
| Line | `#E3E8DF` | Borders and separators |
| Income | `#18734E` | Income values |
| Expense | `#B54747` | Expense values |

Typography uses the system sans-serif stack for reliable rendering. Financial values use tabular numerals. Corners are moderately rounded, borders are quiet, and shadows only distinguish elevated surfaces.

## Layout and hierarchy
- A dark evergreen sidebar anchors desktop navigation.
- The opening view uses a clear editorial heading, a high-contrast balance panel, and three compact period metrics.
- The balance panel is the primary focal point. Its supporting totals remain visible without competing with the balance.
- The cash-flow line chart receives the largest chart area. Composition and category charts remain secondary.
- Transaction entry and the ledger use consistent surface, field, and table patterns.
- Mobile replaces the sidebar with a labeled bottom navigation bar and safe-area spacing.
- At narrow widths, charts and forms become single-column layouts. Header actions remain easy to reach.

## Interaction and accessibility
- All visible controls retain their existing actions and use touch targets of at least 44px.
- Semantic HTML, labels, skip navigation, visible focus, keyboard access, and reduced-motion support are required.
- Empty, error, and success states explain what happened and what the user can do.
- Transaction descriptions render as text, never as HTML.
- Existing LocalStorage records under `financeProData` remain compatible.
- Excel export remains a user-triggered file download, not a live synchronized workbook.

## Design constraints
- Do not use the lime accent as a general-purpose decoration.
- Keep green and red reserved for meaningful financial states.
- Avoid unnecessary animation, gradients, and ornamental charts.
- Preserve legibility and the hierarchy of financial information across screen sizes.
