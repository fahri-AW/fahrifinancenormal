# FinancePro Design Direction

## Product identity
FinancePro is a personal finance ledger for recording daily income and expenses. The primary job is to help a person understand cash flow, identify spending patterns, and keep a reliable transaction history.

## Existing visual direction retained
The current repository establishes a restrained cobalt and navy identity. Keep that identity rather than replacing it with a generic theme.

- Core: cobalt blue `#3157D5` for primary actions and active navigation.
- Structure: deep navy `#172554` for headings and the main balance surface.
- Neutral: cool near-white canvas `#F5F7FB`, white work surfaces, and slate text.
- Semantic: green for income and red for expenses. Never use these colors as decoration.
- Typography: system sans-serif for familiar, fast reading. Tabular numerals for money.
- Shape: modest corner radii. Use borders for grouping and shadows only where a surface needs elevation.

## Composition
- Desktop navigation groups the real destinations: overview, transactions, and reports.
- Mobile navigation becomes a labeled bottom bar with safe-area spacing.
- The opening view prioritizes the current balance and period cash flow.
- Transaction entry and the ledger remain close to the analysis, because recording and reviewing are the core tasks.
- Charts must reflect actual saved transactions. Empty, loading, and error states must explain what happened and what the user can do next.

## Interaction principles
- Every control has a real action, a visible focus state, and a touch target of at least 44px.
- Transaction descriptions are rendered as text, never interpreted as HTML.
- Existing LocalStorage records under `financeProData` remain readable.
- Excel export is a user-triggered copy of the current local data, not a live synchronized workbook.

## Design Read
ENERGY 2 / RHYTHM 3 / MOTION 1.

Energy stays calm because financial records need trust and legibility. Rhythm varies between the balance summary, a dominant cash-flow chart, compact category analysis, the entry form, and the ledger. Motion is limited to short state feedback and respects reduced-motion preferences.

## Visual decisions and purpose
- The navy balance surface is the primary focal point for the user's main decision: whether recorded cash flow is positive.
- Green and red are reserved for income and expense values so their meaning remains consistent.
- A line chart shows change over time; a doughnut shows the split between income and expenses; a horizontal bar chart ranks expense categories.
- The ledger uses aligned monetary values and restrained row separators to support scanning.
