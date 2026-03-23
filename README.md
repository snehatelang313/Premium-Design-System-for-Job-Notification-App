# Job Notification SaaS - Design System Foundation

This repository contains the visual foundation for a serious B2C SaaS product.
It intentionally avoids product features and focuses only on design system building blocks.

## Design Principles

- Calm and intentional
- Confident and coherent
- No flashy decoration
- No gradients
- No glassmorphism
- No neon colors
- No animation noise

## Foundation Scope

- Design tokens (`design-tokens.json`)
- Base styles and component primitives (`design-system.css`)
- Static foundation preview (`index.html`)

## Core Decisions

- Background: `#F7F6F3`
- Primary text: `#111111`
- Accent: deep red `#8B0000`
- Semantic states: muted green for success, muted amber for warning
- High hierarchy headings with serif typography
- Functional sans-serif body text for readability
- Body text size is constrained to `16px-18px` with `1.6-1.8` line-height
- Text blocks are capped at `720px` for readability
- Spacing scale is fixed to `8px, 16px, 24px, 40px, 64px`
- Page shell follows:
  `[Top Bar] -> [Context Header] -> [Primary Workspace 70% + Secondary Panel 30%] -> [Proof Footer]`

## Content

- Subtext under headers: **one line** (use `.subtext`; ellipsis if overflow).
- Copy is **direct and clear**; avoid marketing or hype.

## Primary workspace

- Minimal **cards**, **subtle** borders (`.card` uses `--border-faint`), **no** heavy shadows.
- Predictable patterns and **generous** spacing (e.g. `.workspace-primary` gap `40px`).

## Secondary panel

- Short **step explanation** in plain language.
- **Copyable prompt** block (`.prompt-box`, `.prompt-box__text`) plus copy actions.
- **Panel buttons** use a single shared style (`.btn-panel`).

## Proof footer

- **Checklist** with empty square markers (`.proof-checklist`): UI Built, Logic Working, Test Passed, Deployed.

## Components

- **Primary button**: solid `#8B0000` (`.btn-primary`).
- **Secondary button**: **outlined** only — transparent fill, visible border (`.btn-secondary`).
- **Border radius**: single system radius `--radius-ui` (`10px`) on buttons, inputs, cards, tables, panels, tabs (badges keep `--radius-pill`).
- **Inputs**: clean default border, hover darkens border; **focus** uses accent border + soft ring (`.input`, `.select`, `.textarea`).
- **Cards**: subtle border, **no drop shadows** (`.card`).

## Interaction

- **Transitions**: `175ms` (within 150–200ms), **`ease-in-out`** (`--duration-motion`, `--ease-standard`).
- **No** bounce or elastic motion; **no** parallax.
- **`prefers-reduced-motion`**: duration collapses to `0ms`.

## Error and empty states

- **Errors**: state what went wrong and **how to fix it**; tone is neutral — **never blame the user** (`.alert-error`, `.field-error`, `.field--invalid`).
- **Empty states**: always include **next step** guidance; avoid blank areas (`.empty-state`).

## Confirmation

The foundation in this repo is **cohesive and consistent** with the rules above: shared radius, outlined secondary actions, solid primary CTA at `#8B0000`, restrained motion, and explicit error/empty patterns (see `index.html` + `design-system.css`).

## Notes

This is a foundation-only system. Product workflows, domain features, and business logic are intentionally excluded.
