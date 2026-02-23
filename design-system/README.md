# MDSS Design System

Design tokens and component patterns for **MetaDefender Storage Security**.

> This is a living document — tokens and patterns are added as the prototype evolves.

---

## Files

| File | Purpose |
|------|---------|
| `tokens.json` | Structured design tokens (consumable by Style Dictionary, Figma Tokens, etc.) |
| `tokens.css` | CSS custom properties — drop into any project via `@import` |
| `README.md` | This file — human-readable reference |

---

## Typography

| Token | Value | Usage |
|-------|-------|-------|
| `--font` | `'Roboto', sans-serif` | Body text, UI elements |
| `--font-brand` | `'Simplon Norm', sans-serif` | Logo, branding, sidebar footer |

### Font files (Simplon Norm)
Located in `/fonts/`:
- `simplonnorm-regular-webfont.woff2` (400)
- `simplonnorm-medium-webfont.woff2` (500)
- `simplonnorm-bold-webfont.woff2` (700)

### Scale

| Token | Size | Usage |
|-------|------|-------|
| `--text-xs` | 10px | Logo subtitle |
| `--text-sm` | 12px | Badges, footer tagline, section titles |
| `--text-md` | 13px | Card descriptions, helper text |
| `--text-base` | 14px | Body, labels, inputs, buttons |
| `--text-lg` | 16px | Banner titles, modal headings |
| `--text-xl` | 24px | Page title |

### Weights
- **400** — body text, descriptions
- **500** — labels, buttons, headings
- **700** — logo icon text only

---

## Color Palette

### Core

| Token | Light | Dark | Usage |
|-------|-------|------|-------|
| `--text-strong` | `#0c121d` | `#ffffff` | Primary text |
| `--text-subtle` | `#344565` | `#a9b2c4` | Secondary text |
| `--text-muted` | `#6b7a90` | `#6b7a90` | Placeholder, hint text |
| `--surface-bg` | `#f8f9f9` | `#0c121d` | Page background |
| `--surface-card` | `#ffffff` | `#141b27` | Card background |
| `--border-200` | `#dee0e4` | `#344565` | Input borders, dividers |
| `--border-card` | `#ebecee` | `#24324b` | Card borders |
| `--primary` | `#1d6bfc` | `#4d8dff` | Primary actions, links |
| `--primary-hover` | `#1854c3` | `#3a7df5` | Primary button hover |

### Semantic Colors (Tags / Badges / Verdicts)

| Name | 100 (bg) | 700 (accent) | Text | Usage |
|------|----------|-------------|------|-------|
| Neutral | `#f8f9f9` | `#475b81` | `#0c121d` | Default, informational |
| Inactive | `#f8f9f9` | `#a9b2c4` | `#6b7a90` | Disabled, inactive |
| Secure | `#e0f5f0` | `#006c4c` | `#004d3a` | Verified, secure |
| Success | `#dffff5` | `#00b37a` | `#002318` | Completed, passed |
| Accent | `#e8f0ff` | `#1d6bfc` | `#0d2654` | Active, in-progress |
| Guide | `#ede8ff` | `#7c5ce0` | `#2d1a6e` | Informational, guide |
| Alert | `#ffdfdb` | `#e83b3b` | `#7e001d` | Error, detected, failed |
| Warn | `#ffebde` | `#e87c1e` | `#802b00` | Warning |
| Caution | `#fff4cc` | `#d4a800` | `#5d4200` | Low severity, caution |

---

## Spacing

| Token | Value | Usage |
|-------|-------|-------|
| `--space-2` | 2px | Nav divider margins |
| `--space-4` | 4px | Logo gap, nav list gap |
| `--space-8` | 8px | Header icon gap, input padding-y |
| `--space-12` | 12px | Form row gaps, input padding-x |
| `--space-16` | 16px | Card header desc padding, dropdown items |
| `--space-20` | 20px | Card content padding, banner padding |

---

## Border Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius` | 4px | Buttons, cards, inputs, tabs |
| `--radius-md` | 8px | Dropdowns, popovers |
| `--radius-pill` | 9999px | Toggle switch, notification dot |
| `--radius-circle` | 50% | Avatar, radio buttons |

---

## Shadows

| Token | Value | Usage |
|-------|-------|-------|
| `--shadow-card` | `1px 3px 4px -2px rgba(12,18,29,0.04), ...` | Settings cards |
| `--shadow-dropdown` | `0 4px 16px rgba(12,18,29,0.12), ...` | Dropdowns, popovers |
| `--shadow-toggle` | `0 0 6px -4px rgba(0,0,0,0.48), ...` | Toggle thumb |
| `--shadow-focus` | `0 0 0 3px rgba(29,107,252,0.15)` | Input focus ring |

---

## Sizing

| Element | Value |
|---------|-------|
| Header height | 56px |
| Sidebar width | 260px |
| Sidebar collapsed | 60px |
| Control height | 32px (buttons, inputs) |
| Form label width | 266px |
| Icon size | 18px (header/sidebar), 16px (help/filter) |
| Toggle switch | 28px x 16px |
| Radio circle | 16px |
| Avatar | 32px |

---

## Component Inventory

### Layout
- **Header** — fixed top bar with logo, sidebar toggle, theme toggle, notifications, avatar
- **Sidebar** — collapsible nav with icon-only mode, nav items, dividers, footer with brand
- **Content area** — page title + tab bar + scrollable card stack

### Navigation
- **Tab bar** — horizontal pills, dark active state (`--tab-active-bg`)
- **Nav items** — icon + label, active state uses `#E8F0FF` bg (light) / blue overlay (dark)

### Cards
- **Settings card** — header (56px) + content area, supports dirty state with Save/Discard
- **Pool card** — draggable, with header, table, and action menu

### Forms
- **Form row** — fixed-width label (266px) + flexible value area
- **Input field** — 32px height, border on focus with ring, supports clear/eye icons
- **Select** — native styled with custom chevron
- **Radio group** — vertical list with circle indicators
- **Toggle switch** — 28x16 pill with sliding thumb
- **File upload** — dashed border field

### Buttons
- **Primary** (`btn-primary`) — filled blue, white text
- **Outline** (`btn-outline`) — bordered, transparent bg, supports `.danger` variant
- **Export** (`btn-export`) — primary bg with icon
- **Discard** (`btn-discard`) — only visible in dirty card state
- **Save** (`btn-save`) — disabled by default, activates with dirty state

### Data Display
- **Tags** — status (filled bg) and keyword (bordered) variants, 9 color schemes
- **Badges** — dot (8px circle) and number (16px rounded rect) variants
- **Chips** — 24px height, filled bg, supports selected/removable state
- **Verdicts** — dot + text inline, semantic color mapping
- **Severities** — triangle icon + text, 5 levels (critical → none)
- **Tables** — header with sort/filter icons, hover rows, action column
- **AV badge** — inline badge for antivirus engine names

### Overlays
- **Modal** — centered dialog with header, body, footer, close button
- **Slide-out panel** — right-side drawer (420px), used for add/edit forms
- **Advanced filters drawer** — right-side panel with filter fields
- **Column dropdown** — sort/pin popover on table columns
- **Action menu** — context menu on table rows
- **Toast** — bottom-right snackbar notification
- **Notification toast** — top-right with icon, title, description

### Miscellaneous
- **Promo banner** — blue bg with CTA button
- **Warning banner** — icon + title + description
- **Avatar dropdown** — user menu with settings, language, logout
- **Notification dropdown** — bell icon with badge, scrollable list

---

## Dark Mode

Activated via `data-theme="dark"` on `<html>`. All CSS variables are overridden in a single `[data-theme="dark"]` block. Key changes:

- Surfaces invert: light gray → dark navy
- Text inverts: dark → light
- Primary shifts: `#1d6bfc` → `#4d8dff` (lighter blue for contrast)
- Borders shift: `#ebecee` → `#24324b`
- Semantic colors adjust for dark backgrounds (lighter tints)

---

## WCAG 2.2 AA Compliance

The prototype includes:
- Focus-visible outlines (2px solid primary, 2px offset) on all interactive elements
- Screen-reader only utility class (`.sr-only`)
- `prefers-reduced-motion` support (disables transitions/animations)
- Windows High Contrast Mode (`forced-colors`) support
- ARIA labels on all icon buttons and interactive controls
- Keyboard-accessible radio options, file uploads, and help icons

---

## Pages Implemented

| Page | Tab | Description |
|------|-----|-------------|
| Settings | Profile | User preferences, language, defaults |
| Settings | Notifications | Email/webhook notification rules |
| Settings | Scan Pools | MetaDefender Core pool management |
| Settings | Security | Session, password, 2FA settings |
| Settings | SMTP | Email server configuration |
| Settings | Licensing | License activation and management |
| Settings | SSO | SAML/OIDC SSO configuration |
| Settings | Data | Data retention, cleanup, export |
| Audit | — | Audit log with filters, search, expandable rows |
| Components | — | Design system showcase page |
