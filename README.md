# Attain Concepts Design System

Token-driven CSS design system with primitives, utilities, components, and patterns.

## Structure

- `primitives/` — design tokens + base styles
- `utilities/` — layout helpers (grid, stack, container)
- `components/` — reusable UI components (button, card, badge, etc.)
- `motion/` — transition + easing conventions
- `tokens/` — source-of-truth token JSON (optional; useful if you later add a build step)

## Quick start (static CSS)

1) Include the design system CSS:
```html
<link rel="stylesheet" href="./primitives/index.css">
<link rel="stylesheet" href="./utilities/index.css">
<link rel="stylesheet" href="./motion/index.css">
<link rel="stylesheet" href="./components/index.css">
```

2) Use classes like:
- `.ac-btn.ac-btn--primary`
- `.ac-card`
- `.ac-badge.ac-badge--foundational` (etc.)

## Token workflow

Your tokens live in `primitives/tokens.css`.
- Edit values there.
- Components and utilities only reference semantic tokens.
- Keep token names stable; version breaking changes with semver.

## Versioning

- Patch: bug fixes, docs, non-breaking tweaks
- Minor: new components/tokens (non-breaking)
- Major: renames/removals, token contract changes

## Conventions

- Prefix everything with `ac-` (tokens) / `ac-` (classes) to avoid collisions.
- Prefer semantic tokens (e.g., `--ac-semantic-text-primary`) inside components.
- Motion: no bouncy easing; keep transitions subtle.

---
Generated scaffold for Attain Concepts.
