# MDSS (MetaDefender Storage Security)

MDSS is an OPSWAT product for securing cloud storage. This repo contains the product UI — a single-page HTML application.

**Live:** https://vilevich.github.io/mdss/
**Design system:** https://github.com/vilevich/blue-line

## How It Works

The UI is a single `index.html` file. All design system CSS comes from Blue Line via GitHub Pages:

```html
<link rel="stylesheet" href="https://vilevich.github.io/blue-line/tokens.css">
<link rel="stylesheet" href="https://vilevich.github.io/blue-line/components.css">
<link rel="stylesheet" href="https://vilevich.github.io/blue-line/icons.css">
```

Product-specific styles go in the inline `<style>` block inside `index.html`, after the DS links.

## File Structure

```
index.html     — The entire product UI (all pages, navigation, JS)
README.md      — Project overview
Wordmark.png   — OPSWAT logo
.github/       — GitHub Pages deployment workflow
```

## Pages

| Page | Description |
|------|-------------|
| Settings | 8 tabs: Profile, Scan Pools, Security, SMTP, Notifications, Licensing, SSO, Data |
| Audit | Audit log with filters, search, expandable rows |
| Users | User management with roles and permissions |
| Jobs | Active/upcoming/past scan jobs with detail views |
| Workflows | Workflow list + detail flow diagram with config panels |
| Inventory | Accounts, account detail (units/jobs tabs), settings panel |

## Key Patterns

- **Navigation:** Left sidebar with collapsible sections, page routing via JS
- **Tables:** Uses Blue Line's two-type system (small `.data-table` vs big `.data-table.table-fixed`)
- **Forms:** Blue Line form components (`.form-row`, `.input-field`, `.select-field`, `.toggle-switch`)
- **Overlays:** Modals (`.modal-overlay`) and slide panels (`.slide-panel`)
- **Dark mode:** Toggle in header, uses Blue Line's `data-theme="dark"` system

## Adding New Pages

1. Use Blue Line CSS classes from the design system
2. If a component doesn't exist in Blue Line, build it product-specific first
3. Follow existing page patterns in `index.html` for navigation, layout, and JS routing
4. Test in both light and dark mode
