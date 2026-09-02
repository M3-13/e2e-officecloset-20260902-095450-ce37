# Design — Project Identity

> This document is project-long-lived. Tokens are not changed without
> the Architect's approval. Developers MUST use these tokens
> instead of improvising their own colors/spacings.

## Style Direction

Glamouröser Red-Carpet-Look: tiefes Mitternachtsviolett, Champagner-Gold als Akzent, elfenbeinfarbene Serifen-Typografie und vitrinenartige Bildkacheln – elegant, aber klar bedienbar.

## Colors

- `--color-bg`: **#0E0B12**
- `--color-surface`: **#17121D**
- `--color-fg`: **#F5EFE0**
- `--color-muted`: **#9A8F8A**
- `--color-accent`: **#C9A227**
- `--color-accent_hover`: **#D9B94A**
- `--color-accent_active`: **#A9851E**
- `--color-border`: **#2E2636**
- `--color-danger`: **#E5484D**
- `--color-success`: **#3E9B6F**

## Typography

- `font_family`: Georgia, 'Times New Roman', 'Segoe UI', system-ui, -apple-system, sans-serif
- `heading_weight`: 600
- `body_weight`: 400

## Spacing Scale

- `--space-0`: 4px
- `--space-1`: 8px
- `--space-2`: 12px
- `--space-3`: 16px
- `--space-4`: 24px
- `--space-5`: 32px
- `--space-6`: 48px

## Border-Radii

- `--radius-sm`: 4px
- `--radius-md`: 8px
- `--radius-lg`: 16px
- `--radius-pill`: 999px

## Components

### Button

Primär: bg=accent #C9A227, fg=#1A1420, font-weight 600, padding 12px 24px, radius md 8px, min-height 44px, border 1px solid transparent, transition 150ms. Hover: bg=accent_hover #D9B94A + dezenter goldener Schatten. Active: bg=accent_active #A9851E, translateY(1px). Disabled: opacity 0.45, cursor not-allowed. Sekundär: bg transparent, border 1px solid accent, fg=accent, gleiche Maße.

### Card

bg=surface #17121D, border 1px solid #2E2636, radius lg 16px, padding 16px, box-shadow 0 8px 24px rgba(0,0,0,0.35); Hover: border=accent mit weichem Glow, transition 200ms.

### Input

bg=#120E16, fg=#F5EFE0, border 1px solid #2E2636, radius md 8px, padding 12px 14px, min-height 44px, placeholder=#9A8F8A; Focus: border=accent, box-shadow 0 0 0 3px rgba(201,162,39,0.25); Invalid: border=danger #E5484D.

### Modal

Overlay bg rgba(10,7,13,0.7), backdrop-filter blur(4px), zentriert; Panel bg=surface, radius lg 16px, padding 24px, max-width 480px, border 1px solid #2E2636, box-shadow 0 16px 48px rgba(0,0,0,0.5).

### Nav

Sticky top, bg rgba(14,11,18,0.92), backdrop-filter blur(8px), border-bottom 1px solid #2E2636, height 64px; Links in muted #9A8F8A, aktiv in accent mit 2px goldener Unterstreichung, hover=fg #F5EFE0; Touch-Ziele min 44px.

### Badge

Kategorie-Chip: bg=#221B2B, border 1px solid #2E2636, fg=#9A8F8A, radius pill, padding 6px 12px, font-size 13px; aktiv/gewählt: bg rgba(201,162,39,0.15), border=accent, fg=accent.

### ImageTile

Garderoben-/Outfit-Kachel: Bild aspect-ratio 4/5, object-fit cover, radius md 8px, bg-Fallback #221B2B; darunter Name in fg (font-weight 600) und Kategorie in muted; ganze Kachel min 44px klickbar.

### EmptyState

Zentriert, fg=#9A8F8A, gestrichelte Border #2E2636, radius lg 16px, padding 32px; primärer CTA-Button zentriert darunter.

## Layout Principles

- Container max-width 1200px, horizontal zentriert; Seitenabstand 16px mobil, 32px ab 1024px.
- Breakpoints: 640px (mobil) und 1024px (Tablet/Desktop).
- Garderobe und gespeicherte Outfits als responsives CSS-Grid: grid-template-columns repeat(auto-fill, minmax(180px, 1fr)), gap 24px; mobil 2 Spalten mit minmax(140px, 1fr).
- Vertikaler Abstand zwischen Sektionen 48px, innerhalb von Sektionen 24px.
- Navigation bleibt sticky oben erreichbar; primäre Aktionen (Anlegen, Speichern) stehen rechts oder als deutlicher CTA.
