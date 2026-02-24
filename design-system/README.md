# MDSS Design System

Design tokens and component patterns for **MetaDefender Storage Security**.

> Extracted from Figma Blue Line 2.2.2. This is a living system — tokens and components are added as the prototype evolves.

---

## Quick Start

Add these two `<link>` tags to any HTML page **before** your product-specific `<style>`:

```html
<link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;500;700&display=swap" rel="stylesheet">
<link rel="stylesheet" href="design-system/tokens.css">
<link rel="stylesheet" href="design-system/components.css">
```

Everything cascades automatically — product-specific overrides go in your inline `<style>` after the links.

---

## Files

| File | Purpose |
|------|---------|
| `tokens.css` | CSS custom properties, `@font-face`, dark mode variable overrides, body base styles |
| `components.css` | All reusable component styles with colocated dark mode overrides |
| `tokens.json` | Structured design tokens (consumable by Style Dictionary, Figma Tokens, etc.) |
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
| `--size-h1` | 32px | Page hero titles |
| `--size-h2` | 24px | Page titles |
| `--size-h3` | 20px | Section headings |
| `--size-h4` | 16px | Card titles, banner titles, modal headings |
| `--size-label` | 14px | Body, labels, inputs, buttons |
| `--size-paragraph` | 14px | Body paragraphs, descriptions |
| `--size-note` | 12px | Badges, footer tagline, small text |
| `--size-inset` | 10px | Logo subtitle |

### Weights
- **400** — body text, descriptions
- **500** — labels, buttons, headings

### Line Heights
| Token | Value |
|-------|-------|
| `--lh-h1` | 36.48px |
| `--lh-h2` | 27.36px |
| `--lh-h3` | 22.8px |
| `--lh-h4` | 18.24px |
| `--lh-body` | 15.96px |
| `--lh-body-paragraph` | 18.62px |
| `--lh-note` | 13.68px |
| `--lh-note-paragraph` | 15.96px |
| `--lh-inset` | 11.4px |

---

## Color Palette

Full scales from Figma Blue Line 2.2.2:

| Scale | Range | Example |
|-------|-------|---------|
| Neutral | 100–1200 + white | `--neutral-700: #475b81` |
| Blue | 100–1100 | `--blue-700: #1d6bfc` |
| Red | 100–1000 | `--red-800: #d40031` |
| Green | 100–1200 | `--green-1000: #006c4c` |
| Orange | 100–1100 | `--orange-700: #ff6b00` |
| Yellow | 100–1200 | `--yellow-700: #dbb600` |
| Teal | 100–1200 | `--teal-600: #03e7f5` |
| Purple | 100–1000 | `--purple-700: #9f2caa` |

### Semantic Aliases

| Token | Light | Dark | Usage |
|-------|-------|------|-------|
| `--text-strong` | `neutral-1200` | `#ffffff` | Primary text |
| `--text-subtle` | `neutral-800` | `neutral-500` | Secondary text |
| `--text-muted` | `neutral-600` | `neutral-600` | Placeholder, hint text |
| `--surface-bg` | `neutral-100` | `neutral-1200` | Page background |
| `--surface-card` | `neutral-white` | `neutral-1100` | Card background |
| `--border-200` | `neutral-300` | `neutral-800` | Input borders, dividers |
| `--border-card` | `neutral-200` | `neutral-900` | Card borders |
| `--primary` | `blue-700` | `#4d8dff` | Primary actions, links |
| `--primary-hover` | `blue-800` | `#3a7df5` | Primary button hover |

### DS Semantic Colors (Tags / Badges / Verdicts)

| Name | 100 (bg) | 700 (accent) | Text | Usage |
|------|----------|-------------|------|-------|
| Neutral | `neutral-100` | `neutral-700` | `neutral-1200` | Default, informational |
| Inactive | `neutral-100` | `neutral-500` | `neutral-600` | Disabled, inactive |
| Secure | `green-100` | `green-1000` | `green-1200` | Verified, secure |
| Success | `green-100` | `green-800` | `green-1200` | Completed, passed |
| Accent | `blue-100` | `blue-700` | `blue-1000` | Active, in-progress |
| Guide | `#ede8ff` | `purple-700` | `#2d1a6e` | Informational, guide |
| Alert | `red-100` | `red-700` | `red-1000` | Error, detected, failed |
| Warn | `orange-100` | `orange-700` | `orange-1000` | Warning |
| Caution | `yellow-100` | `yellow-700` | `yellow-1000` | Low severity, caution |

---

## Spacing

| Token | Value | Usage |
|-------|-------|-------|
| `--space-none` | 0px | — |
| `--space-tiny` | 2px | Nav divider margins |
| `--space-tight` | 4px | Logo gap, nav list gap |
| `--space-xs` | 8px | Header icon gap, input padding-y |
| `--space-sm` | 12px | Form row gaps, input padding-x |
| `--space-std` | 20px | Card content padding, banner padding |
| `--space-double` | 40px | Large section gaps |
| `--space-gutter` | 12px | Default gutter |
| `--space-gutter-compact` | 8px | Compact gutter |

---

## Corner Radius

| Token | Value | Usage |
|-------|-------|-------|
| `--radius-none` | 0px | No rounding |
| `--radius` | 4px | Buttons, cards, inputs, tabs |
| `--radius-graphics` | 8px | Dropdowns, popovers |
| `--radius-modals` | 12px | Modal dialogs |
| `--radius-circular` | 9999px | Toggle switch, pills, notification dot |

---

## Elevation / Shadows

| Token | Usage |
|-------|-------|
| `--shadow-1` | Subtle elevation |
| `--shadow-2` | Medium elevation |
| `--shadow-3` | High elevation |
| `--shadow-4` | Highest elevation |
| `--shadow-card` | Settings / data cards |

---

## Breakpoints

| Token | Value | Range |
|-------|-------|-------|
| `--screen-lg` | 1920px | Large: 1461–1920 |
| `--screen-md` | 1440px | Medium: 1025–1460 |
| `--screen-sm` | 1024px | Small: 769–1024 |
| `--screen-tb` | 768px | Tablet Portrait: ≤768 |

---

## Component Inventory

### Buttons

All buttons share: `height: 32px`, `font-size: 14px`, `font-weight: 500`, `border-radius: var(--radius)`, `font-family: var(--font)`

| Class | Style | Usage |
|-------|-------|-------|
| `.btn-primary` | Filled blue | Main CTA (Activate, Add, Confirm) |
| `.btn-outline` | Bordered | Secondary action (Cancel, Generate) |
| `.btn-outline.danger` | Bordered red | Destructive secondary action |
| `.btn-text` | No border, blue text | Tertiary action |
| `.btn-text.danger` | No border, red text | Destructive tertiary action |
| `.btn-brand` | Gradient fill | Brand CTA |
| `.btn-icon` | 32x32 bordered square | Icon-only button |
| `.btn-danger` | Filled red | Destructive primary action |
| `.btn-save` | Disabled by default, activates on dirty | Card save button |
| `.btn-discard` | Hidden by default, shows on dirty | Card discard button |

**States:** `:disabled` / `.disabled` (opacity 0.4), `:focus-visible` (blue outline), `.btn-loading` (spinner animation)

### Forms

| Class | Description |
|-------|-------------|
| `.form-row` | Horizontal form layout (`display: flex; gap: 12px`) |
| `.form-label` | Fixed 266px label |
| `.input-field` | Standard text input (32px height) |
| `.select-field` | Styled native select |
| `.input-with-suffix` | Input + suffix unit (e.g. "days") |
| `.radio-group` / `.radio-option` | Radio button group |
| `.toggle-switch` | 28x16 toggle switch |
| `.file-upload-field` | Click-to-browse file input |
| `.help-icon` | 16px tooltip trigger icon |

### Cards

| Class | Description |
|-------|-------------|
| `.audit-card` | Base card (bg, border, shadow, radius) |
| `.audit-card-header` | 56px header with title + actions |
| `.audit-card-header.with-desc` | Header with description text |
| `.card-body` | 20px padded content area |
| `.audit-card-title-editable` | Editable inline title |
| `.card-bulk-actions` | Multi-select bulk action bar |
| `.column-vis-trigger` | Column visibility dropdown button |
| `.card-filter-bar` / `.card-filter-chip` | Filter chip bar |
| `.card-actions-dropdown` | Actions menu trigger |
| `.audit-card-header.selected` | Blue background for multi-select state |

### Tables

| Class | Description |
|-------|-------------|
| `.data-table` | Generic data table (`border-collapse: separate`) |
| `.audit-table` | Audit-specific table with column classes |
| `.filter-icon` | Column sort/filter icon |
| `.col-dropdown` | Sort/pin popover menu |
| `.cell-action` | Table row action icon |
| `.col-pinned` | Sticky column (`position: sticky; left: 0`) with right border stroke |
| `.audit-user` | User cell layout (`display: flex; gap: 8px`) |
| `.audit-avatar` | 24px circular avatar with fallback initial + `.system` variant |

**Sticky / Pinned Columns:** Add `.col-pinned` to any `<th>`/`<td>` to pin it to the left edge during horizontal scroll. The outermost pinned column receives a `border-right` separator. `thead th.col-pinned` automatically gets `z-index: 3` so it stays above body cells. Hover, selected, and dark-mode background states are included.

**Table padding:** First and last columns automatically receive `padding-left: 20px` / `padding-right: 20px` for outer gutter spacing.

### Search & Filter

| Class | Description |
|-------|-------------|
| `.audit-search` | Search input with icon |
| `.audit-filter-btn` | Filter toggle button |

### Pagination

| Class | Description |
|-------|-------------|
| `.audit-pagination` | Pagination bar (56px height, compact padding) |
| `.audit-page-btn` | Page navigation button |
| `.audit-page-select` | Page number select |

### Tags / Badges / Chips / Verdicts / Severities

**Tags** — 9 semantic colors: `.tag-neutral`, `.tag-inactive`, `.tag-secure`, `.tag-success`, `.tag-accent`, `.tag-guide`, `.tag-alert`, `.tag-warn`, `.tag-caution`

**Keyword Tags** — `.tag-keyword` (bordered, no fill)

**Badge Dots** — `.badge-dot-{color}` (8px circles)

**Badge Numbers** — `.badge-number-{color}` (16px rounded rectangles)

**Chips** — `.chip-{variant}` (24px height, filled) + `.chip-selected` with `.chip-remove`

**Verdicts** — `.verdict-{state}` with `.verdict-dot` + `.verdict-text`

**Severities** — `.severity-{level}` with `.severity-icon` (critical, high, medium, low, none)

### Level & Category Badges

| Class | Description |
|-------|-------------|
| `.level-badge` | Inline pill badge (20px height, 10px padding, rounded) |
| `.level-badge.warning` | Caution-themed (yellow bg, dark text) |
| `.level-badge.error` | Alert-themed (red bg, dark text) |
| `.level-badge.info` | Info-themed (teal bg, dark text) |
| `.level-badge.success` | Success-themed (green bg, dark text) |
| `.category-badge` | Bordered pill badge (no fill, neutral border + text) |

Uses `--ds-*` semantic tokens — auto-adapts to dark mode.

### Utility Components

| Class | Description |
|-------|-------------|
| `.expand-btn` | 24×24 icon button for expand/collapse (chevron rotates via `.open`) |
| `.theme-toggle` | 32×32 icon button for light/dark mode switching |
| `.page-view` | View switcher bar (card/table) with `.active` state |
| `.table-page` | Table-page wrapper (card border, radius, shadow) |
| `.priority-toggle` | Segmented toggle bar (e.g. All / Active / Archived) |
| `.priority-toggle-btn` | Individual toggle segment with `.active` state |

### Overlays

| Class | Description |
|-------|-------------|
| `.modal-overlay` / `.modal` | Centered dialog |
| `.slide-panel-overlay` / `.slide-panel` | Right-side drawer (400px) |
| `.panel-field` | Field layout for slide panels |

### Advanced Filters Panel

| Class | Description |
|-------|-------------|
| `.advanced-filters-overlay` | Full-screen backdrop (`rgba(0,0,0,0.25)`) |
| `.advanced-filters-panel` | Right-side drawer (400px, slide-in transition) |
| `.af-header` | Panel header with title + close button |
| `.af-close` | 32×32 close icon button |
| `.af-body` | Scrollable content area (`flex: 1; overflow-y: auto`) |
| `.af-section` | Grouped filter section with bottom border |
| `.af-section-title` | Section heading (12px uppercase, neutral-600) |
| `.af-field` | Two-column grid layout (`grid-template-columns: 1fr 1fr`) |
| `.af-field-label` | Field label text |
| `.af-chips` | Wrapped chip container (`display: flex; flex-wrap: wrap; gap: 6px`) |
| `.af-chip` | Selectable filter chip (bordered pill) + `.selected` state |
| `.af-footer` | Sticky footer with action buttons |

### Dropdown Menus

#### Avatar Dropdown

| Class | Description |
|-------|-------------|
| `.avatar-dropdown-wrap` | Positioning wrapper (`position: relative`) |
| `.avatar-dropdown` | Dropdown panel (280px, shadow-3, hidden by default) |
| `.avatar-dropdown.open` | Visible state (`opacity: 1; pointer-events: auto`) |
| `.avd-user` | User info block (avatar + name + email) |
| `.avd-divider` | Horizontal separator line |
| `.avd-group` | Grouped menu section |
| `.avd-item` | Menu item row (icon + text + optional chevron) |
| `.avd-submenu` | Nested submenu view (slides in on click) |
| `.avd-back` | Back button for submenu navigation |
| `.avd-flag` | 20×14 flag icon for language selection |
| `.avd-check` | Checkmark icon for selected state |

#### Notification Dropdown

| Class | Description |
|-------|-------------|
| `.notif-dropdown-wrap` | Positioning wrapper |
| `.notif-dropdown` | Dropdown panel (380px, shadow-3, hidden by default) |
| `.notif-dropdown.open` | Visible state |
| `.notif-header` | Header bar with title + "Mark all read" action |
| `.notif-list` | Scrollable message list (`max-height: 360px`) |
| `.notif-msg` | Individual notification message |
| `.notif-msg-title` | Message title text |
| `.notif-msg-dot` | Unread indicator dot (8px blue circle) |
| `.notif-msg-body` | Message body text (neutral-700, 12px) |
| `.notif-msg-time` | Timestamp text |
| `.notif-divider` | Message separator |
| `.notif-empty` | Empty state illustration container |
| `.notif-empty-icon` | Empty state icon (80px) |
| `.notif-empty-title` / `.notif-empty-subtitle` | Empty state text |

### Toasts

| Class | Description |
|-------|-------------|
| `.toast` | Bottom-right snackbar |
| `.top-toast` | Top-right notification with icon + title + description |

### Miscellaneous

| Class | Description |
|-------|-------------|
| `.banner` | Warning banner with icon |
| `.status-dot` | 8px colored status circle |
| `.av-badge` | AV engine name badge |
| `.copy-btn` | Copy action icon |
| `.tooltip-popover` | Floating tooltip |
| `.header-icon` | 32×32 header toolbar icon button (ghost style, hover bg) |
| `.notif-dot` | 8px notification indicator dot (positioned top-right of parent) |
| `.header-avatar` | 28×28 circular avatar for header toolbar |
| `.skip-link` | WCAG skip-to-content link |
| `.sr-only` | Screen-reader only utility |

---

## Dark Mode

Activated via `data-theme="dark"` on `<html>`. All semantic variables are overridden in `tokens.css`. Component-level dark overrides are colocated in `components.css`.

Key changes:
- Surfaces invert: light gray → dark navy
- Text inverts: dark → light
- Primary shifts: `#1d6bfc` → `#4d8dff` (lighter blue for contrast)
- Borders shift: `neutral-200` → `neutral-900`
- Shadows increase opacity for dark backgrounds
- Semantic DS colors adjust for dark backgrounds

---

## WCAG 2.2 AA Compliance

Included in `components.css`:
- Focus-visible outlines (2px solid primary, 2px offset) on all interactive elements
- Screen-reader only utility class (`.sr-only`)
- `prefers-reduced-motion` support (disables transitions/animations)
- Windows High Contrast Mode (`forced-colors`) support
- WCAG 2.5.8 minimum target sizes
- Contrast-adjusted placeholder text (#566479 passes 4.5:1 on white)

---

## Responsive Breakpoints

Handled in `components.css`:

| Breakpoint | Behavior |
|-----------|----------|
| ≤1460px | Content padding adjustment |
| ≤1024px | Forms stack vertically, tabs scroll |
| ≤768px | Full responsive: forms, modals, tables adapt |
| ≤480px | Compact spacing for small screens |

---

## Pages Implemented

| Page | Tab | Description |
|------|-----|-------------|
| Settings | Profile | User preferences, language, defaults |
| Settings | Scan Pools | MetaDefender Core pool management |
| Settings | Security | Session, password, 2FA settings |
| Settings | SMTP | Email server configuration |
| Settings | Notifications | Email/webhook notification rules |
| Settings | Licensing | License activation and management |
| Settings | SSO | SAML/OIDC SSO configuration |
| Settings | Data | Data retention, cleanup, export |
| Audit | — | Audit log with filters, search, expandable rows |
| Users | — | User management with roles and permissions |
| Jobs | — | Scan job management with detail views |
| Components | — | Design system showcase page |
