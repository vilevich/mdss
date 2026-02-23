# MetaDefender Storage Security — UI Prototype

Interactive HTML prototype for the MDSS Settings, Audit, and Components pages.

**Live preview:** https://vilevich.github.io/mdss-ui-prototype/

---

## Quick Start

Open `index.html` in a browser, or serve locally:

```bash
npx serve -l 3000 .
```

---

## Project Structure

```
├── index.html              # Full prototype (all pages, interactions, dark mode)
├── Wordmark.png            # OPSWAT brand logo
├── fonts/                  # Simplon Norm webfont files (woff2)
├── design-system/
│   ├── README.md           # Human-readable design system reference
│   ├── tokens.json         # Structured design tokens (JSON)
│   └── tokens.css          # CSS custom properties (importable)
└── README.md               # This file
```

---

## What's Included

### Pages
- **Settings** — 8 tabs: Profile, Notifications, Scan Pools, Security, SMTP, Licensing, SSO, Data
- **Audit** — Log table with search, advanced filters drawer, expandable detail rows
- **Components** — Design system showcase (tags, badges, chips, verdicts, severities)

### Features
- Fully interactive (tab switching, toggle states, modals, slide-out panels, drag-and-drop)
- Dark mode toggle (top-right)
- Responsive layout (tablet + mobile breakpoints)
- WCAG 2.2 AA accessibility (focus management, ARIA, reduced motion, high contrast)
- Collapsible sidebar with icon-only mode

---

## Design System

All design tokens are documented in [`design-system/`](./design-system/):

| File | Description |
|------|-------------|
| [`tokens.css`](./design-system/tokens.css) | CSS custom properties — import directly into your project |
| [`tokens.json`](./design-system/tokens.json) | Structured tokens — use with Style Dictionary, Figma Tokens, etc. |
| [`README.md`](./design-system/README.md) | Full reference: colors, typography, spacing, components, dark mode |

---

## For Developers

### How to use this prototype

1. **Browse the live site** to understand interactions and states
2. **Inspect elements** in DevTools — all components use semantic class names
3. **Reference the design system** in `design-system/` for exact token values
4. **View source** — the HTML is organized with section comments (`<!-- === SECTION === -->`)

### Key conventions

- All sizing uses `32px` control height (buttons, inputs, selects)
- Form layout: `266px` fixed label + flexible value area
- Cards: `56px` header height, `20px` content padding
- `4px` border-radius on everything except dropdowns (`8px`) and pills (`9999px`)
- Dark mode: toggle `data-theme="dark"` on `<html>` — all tokens auto-switch

### Component class naming

| Component | Class pattern |
|-----------|---------------|
| Buttons | `.btn-primary`, `.btn-outline`, `.btn-outline.danger` |
| Inputs | `.input-field`, `.select-field` |
| Tags | `.tag.tag-{variant}`, `.tag-keyword` |
| Badges | `.badge-dot.badge-dot-{variant}`, `.badge-number.badge-number-{variant}` |
| Chips | `.chip.chip-{variant}`, `.chip-selected` |
| Verdicts | `.verdict.verdict-{variant}` |
| Severities | `.severity.severity-{level}` |
| Cards | `.settings-card`, `.pool-card` |
| Tables | `.pool-table`, `.data-table`, `.audit-table`, `.headers-table` |

---

## Feedback

Please use **GitHub Issues** on this repo to leave feedback:

- **Bug / mismatch** — something doesn't match the intended design
- **Question** — need clarification on a component or interaction
- **Suggestion** — ideas for improvement

When filing an issue, please include:
1. Which page/tab you're looking at
2. Screenshot or screen recording if visual
3. Browser + viewport size if it's a responsive issue

---

## Status

| Area | Status |
|------|--------|
| Settings pages | Done |
| Audit page | Done |
| Component showcase | Done |
| Dark mode | Done |
| Responsive | Done |
| Accessibility (WCAG 2.2 AA) | Done |
| Design tokens extracted | Done |
