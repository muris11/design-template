---
name: design-template-profesional
description: "Profesional Serif — ivory #FAFAF8 + black #1A1A1A + gold #B8860B, Playfair Display + Source Sans 3 + IBM Plex Mono, editorial timeless. Use when user wants profesional, serif, editorial, ivory, timeless, luxury book, literary, refined."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-profesional

> Serif — Typographic elegance through classical restraint. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-profesional design-template-<nama>`.

---

<role>
You are an expert frontend engineer, UI/UX designer, visual design specialist, and typography expert. Your goal is to help the user integrate a design system into an existing codebase in a way that is visually consistent, maintainable, and idiomatic to their tech stack.

Before proposing or writing any code, first build a clear mental model of the current system:
- Identify the tech stack (e.g. React, Next.js, Vue, Tailwind, shadcn/ui, etc.).
- Understand the existing design tokens (colors, spacing, typography, radii, shadows), global styles, and utility patterns.
- Review the current component architecture (atoms/molecules/organisms, layout primitives, etc.) and naming conventions.
- Note any constraints (legacy CSS, design library in use, performance or bundle-size considerations).

Ask the user focused questions to understand the user's goals. Do they want:
- a specific component or page redesigned in the new style,
- existing components refactored to the new system, or
- new pages/features built entirely in the new style?

Once you understand the context and scope, do the following:
- Propose a concise implementation plan that follows best practices, prioritizing:
  - centralizing design tokens,
  - reusability and composability of components,
  - minimizing duplication and one-off styles,
  - long-term maintainability and clear naming.
- When writing code, match the user's existing patterns (folder structure, naming, styling approach, and component patterns).
- Explain your reasoning briefly as you go, so the user understands *why* you're making certain architectural or design choices.

Always aim to:
- Preserve or improve accessibility.
- Maintain visual consistency with the provided design system.
- Leave the codebase in a cleaner, more coherent state than you found it.
- Ensure layouts are responsive and usable across devices.
- Make deliberate, creative design choices (layout, motion, interaction details, and typography) that express the design system's personality instead of producing a generic or boilerplate UI.

</role>

<design-system>
# Design Style: Serif

## Design Philosophy

### Core Principle

**Typographic elegance through classical restraint.** This design system draws inspiration from the finest editorial publications, literary magazines, and luxury brand identities. It believes that the highest form of design is one that elevates content through refined typography, considered spacing, and deliberate simplicity.

The serif typeface is not merely a font choice—it is the soul of this aesthetic.

### The Visual Vibe

**Editorial. Timeless. Warm. Refined.**

Imagine opening a beautifully designed hardcover book or premium architecture magazine. Pages breathe. Typography speaks. Nothing screams—everything placed with intention.

**Emotional Keywords:** Timeless, Warm, Sophisticated, Literary, Confident

Visual signatures: Massive serif headlines, tight letter-spacing `-0.02em`, wide label spacing `0.1-0.2em`, bleed edge on mobile, underlines primary affordance, sharp `0px`.

### The DNA

1. Signature Serif Playfair Display high contrast ball terminals classical proportions — elegant yet contemporary, warm.
2. Warm Palette Ivory #FAFAF8 + Rich Black #1A1A1A + Warm Gray #6B6B6B + Burnished Gold #B8860B gold leaf gilded edge.
3. Rule Line System Thin 1px #E8E4DF horizontal rules, card top accent, underline, table separators editorial rhythm.
4. Small Caps `IBM Plex Mono 0.75rem 0.15em uppercase` + wide tracking + `Source Sans 3` body.
5. Generous Whitespace `py-32→44` `max-w-5xl` `line-height 1.75` whitespace active.
6. Asymmetric Balance `1.3fr/0.7fr` Benefits, centered hero offset decor.

---

## Design Token System

### Color Strategy

| Token | Value | Usage |
| background | #FAFAF8 | Ivory warm |
| foreground | #1A1A1A | Rich black |
| muted | #F5F3F0 | Card bg warm |
| muted-foreground | #6B6B6B | Secondary warm gray |
| accent | #B8860B | Burnished gold |
| accent-secondary | #D4A84B | Lighter gold gradient/hover |
| accent-foreground | #FFFFFF | On gold |
| border | #E8E4DF | Warm gray rules |
| card | #FFFFFF | Pure white lift |
| ring | #B8860B | Focus gold |

### Typography System

**Font Pairing:** Display/Headlines `"Playfair Display"` serif, Body/UI `"Source Sans 3"` sans, Monospace `"IBM Plex Mono"` labels.

**Type Scale:**

| Element | Size | Font | Weight | Tracking | Notes |
| Hero Headline | `7xl→4.5rem` | Playfair | Normal | `-0.02em` | tight 1.1 centered |
| Section Headlines | `4xl→2.5rem` | Playfair | Normal | `-0.01em` | 1.2 |
| Card Titles | `xl→1.25rem` | Playfair | Semibold | Normal | 1.3 |
| Body | `base→lg` | Source Sans 3 | Normal | `0.01em` | 1.75 relaxed |
| Labels | `xs 12px` | IBM Plex Mono | Medium | `0.15em` | UPPERCASE |

**Small Caps Pattern:**
```
.small-caps { font-family: IBM Plex Mono; font-size: 0.75rem; font-weight: 500; letter-spacing: 0.15em; text-transform: uppercase; }
```

### Spacing & Layout

Luxurious breathing room. Section `py-32→44`, Container `max-w-5xl` narrow readable, Component `p-8→10`, Gap `8→12`.

Layout: Hero centered narrow stacked, Features 3-col `gap-8` generous, Benefits asymmetric `1.3fr/0.7fr`, Rule lines structure.

### Borders, Surfaces & Shadows

Surfaces `card #FFFFFF` lift from ivory, `border 1px #E8E4DF` thin warm, Shadows `shadow-sm 0 1px 2px rgba(26,26,26,0.04)` → `sm→md→lg`, Rule lines critical: thin horizontal `#E8E4DF` + Top accent `2px #B8860B` + decorative under headline.

---

## Component Styling & Interactions

### Buttons

Primary: `accent gold #B8860B` white medium tracked `rounded-md 6px` subtle `shadow-sm` accent-tinted hover `accent-secondary` `shadow-accent` lift `-0.5` active `0`. Secondary: Transparent `border 1px foreground` → hover `muted bg + accent` color. Ghost: `muted-foreground→foreground` underline `accent` `4px`.

Animation refined `200ms` lift tactile.

### Cards

Standard: `card white border 1px border rounded-lg 8px shadow-sm p-6→8` top accent optional `2px accent`, Hover `shadow-md border-hover bg-muted/30` no translate, Elevated `shadow-md`, Featured `accent-muted 6% + 2px accent top + elevated`.

### Inputs

`h-12 border 1px input rounded-md transparent` Hover `border-hover`, Focus `ring-2 ring-accent ring-offset-2 border-accent 150ms`, placeholder `muted-foreground/60` sans base.

### Section Labels

```jsx
<div className="mb-6 flex items-center gap-4">
  <span className="h-px flex-1 bg-[var(--border)]" />
  <span className="font-mono text-xs font-medium uppercase tracking-[0.15em] text-[var(--accent)]">Section Name</span>
  <span className="h-px flex-1 bg-[var(--border)]" />
</div>
```

## The "Bold Factor" (Signature Elements)

1. Dramatic Serif Headlines `7xl` scale beauty not decoration.
2. Rule Line System thin horizontal rhythm editorial.
3. Small Caps `0.15em` tracked uppercase mono.
4. Burnished Gold single warm accent.
5. Generous Whitespace `py-32→44` premium not cramped.
6. Large Display Numbers `5xl+` serif.
7. Decorative Quote Marks large accent gold.
8. Asymmetric Layouts `1.3fr/0.7fr`.
9. Layered Depth: gradient `from-[color] via to` + decorative ring/circle low opacity + multi-layer card + hover interactive + accent tints.
10. Paper Texture overlay `30%` noise subtle print tactile.
11. Ambient Glow blurred circle `2%` warm depth.
12. Micro-interactions: Button lift, Card background tint, Border shift `200ms`.

## Effects & Animation

Restrained refined. `transition-all 200ms ease-out` `150ms` subtle. Hover brightness 5-10%, shadow enhance, underlines. No translate/lift trendy. Entrance fade `opacity 0→1 0.6s easeOut`.

## Responsive Strategy

Mobile (<768): Hero centered `text-[2.5rem]` vertical stack CTAs full-width, Stats 2-col (4 desktop) `text-4xl`, Features/Testimonials/Blog single→stack gap-8, Pricing stacked highlighted loses translate but keeps tint, Nav logo `text-lg→xl` hidden, Buttons `min-h-[44px]` touch-manipulation, Padding `py-32→py-20` `gap-8→6`, Headlines `text-[2.5rem]` serif soul intact.

## Accessibility

WCAG AA, rich black ivory AAA, gold passes white, focus `ring-2 ring-accent ring-offset-2` offset, `touch-manipulation`, base 16px `1.75`, AAA 44px.

## Implementation Notes

Tailwind v4, Plus Jakarta? no — Playfair/Source/IBM Plex, Lucide sparse thin 1-2px, noise + vertical writing custom CSS, etc.

For full verbose spec see git history — this distilled keeps tokens identical.

</design-system>

---

## How to use this skill

- Load `design-template-profesional` when task is serif editorial ivory/gold.
- Signature: Ivory #FAFAF8 + Gold #B8860B + Playfair Display + rule lines.

## Profesional Checklist

- [ ] Palette `#FAFAF8` + `#1A1A1A` + `#B8860B` gold single accent.
- [ ] Typography Playfair Display `7xl` + Source Sans 3 body + IBM Plex Mono small caps `0.15em`.
- [ ] Rule lines `h-px` + accent `2px` + small caps rhythm.
