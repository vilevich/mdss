# MetaDefender Storage Security (MDSS)

OPSWAT product for securing cloud storage — scanning, monitoring, and protecting files across storage providers.

**Live:** https://vilevich.github.io/mdss/
**Design System:** [Blue Line](https://github.com/vilevich/blue-line) ([docs](https://vilevich.github.io/blue-line/))

---

## Quick Start

Open `index.html` in a browser, or serve locally:

```bash
npx serve -l 3000 .
```

---

## Pages

| Page | Description |
|------|-------------|
| **Settings** | 8 tabs: Profile, Scan Pools, Security, SMTP, Notifications, Licensing, SSO, Data |
| **Audit** | Log table with search, advanced filters, expandable detail rows |
| **Users** | User management with roles and permissions |
| **Jobs** | Active/upcoming/past scan jobs with detail views |
| **Workflows** | Workflow list + detail flow diagram with config panels |
| **Inventory** | Accounts, account detail (units/jobs tabs), settings panel |

---

## Design System

MDSS uses the [Blue Line](https://github.com/vilevich/blue-line) design system, loaded via GitHub Pages:

```html
<link rel="stylesheet" href="https://vilevich.github.io/blue-line/tokens.css">
<link rel="stylesheet" href="https://vilevich.github.io/blue-line/components.css">
<link rel="stylesheet" href="https://vilevich.github.io/blue-line/icons.css">
```

Product-specific styles are in the inline `<style>` block inside `index.html`.

---

## Features

- Fully interactive (tab switching, toggle states, modals, slide-out panels)
- Dark mode toggle (top-right header)
- Responsive layout (tablet + mobile breakpoints)
- WCAG 2.2 AA accessibility (focus management, ARIA, reduced motion, high contrast)
- Collapsible sidebar with icon-only mode
