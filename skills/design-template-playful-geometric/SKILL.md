---
name: design-template-playful-geometric
description: "Playful Geometric — cream #FFFDF5, violet #8B5CF6, pink #F472B6, amber #FBBF24, emerald #34D399, Outfit + hard shadows, sticker, memphis. Use when user wants playful, geometric, memphis, sticker, pop, tactile, confetti."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-playful-geometric

> Playful Geometric — Stable Grid, Wild Decoration. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-playful-geometric design-template-<nama>`.

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
# Playful Geometric Design System

## Design Philosophy

**Playful Geometric** is the antidote to sterile, corporate minimalism. It creates an emotional connection through **optimism, clarity, and tactile fun**.

The core concept is **"Stable Grid, Wild Decoration"**. The content itself (text, forms) lives in clean, readable areas, but the world around it is alive with movement and shape. It references the **Memphis Group** (80s) but cleans it up for modern digital screens—removing the chaos while keeping the energy.

### The Vibe
**Friendly. Tactile. Pop. Energetic.**
It feels like a playground or a well-organized sticker book. It invites clicking. It smiles at you.

### Visual Signatures
- **Primitive Shapes**: Circles, triangles, squares, pill shapes, and squiggles used as background elements, masks, or icons.
- **Hard Shadows**: Elements often have a hard, offset drop shadow (no blur) giving a sticker or cut-out paper feel.
- **Pattern Fills**: Polka dots, grid lines, and diagonal stripes used to fill shapes or backgrounds.
- **Varied Radii**: Mixing fully rounded corners with sharp ones to create "leaf" shapes or asymmetric blobs.

---

## Design Token System

### Colors (Light Mode)
A punchy, high-saturation palette anchored by strong neutrals.

```
background:        #FFFDF5    // Warm Cream/Off-White (Paper feel)
foreground:        #1E293B    // Slate 800 (Softer than black)
muted:             #F1F5F9    // Slate 100
mutedForeground:   #64748B    // Slate 500
accent:            #8B5CF6    // Vivid Violet (Primary Brand)
accentForeground:  #FFFFFF    // White
secondary:         #F472B6    // Hot Pink (Playful pop)
tertiary:          #FBBF24    // Amber/Yellow (Optimism)
quaternary:        #34D399    // Emerald/Mint (Freshness)
border:            #E2E8F0    // Slate 200
input:             #FFFFFF    // White
card:              #FFFFFF    // White
ring:              #8B5CF6    // Violet Focus
```

**Usage Rule**: Use `accent` for primary actions. Use `secondary`, `tertiary`, and `quaternary` rotationally for decorative shapes, icons, or emphasized words to create a "confetti" effect.

### Typography

**Headings**: `"Outfit", system-ui, sans-serif` - Geometric sans with character. Rounded corners on letters make it friendly. Weights Bold 700 or ExtraBold 800.

**Body**: `"Plus Jakarta Sans", system-ui, sans-serif` - Highly legible, modern, geometric but humanist. Regular 400, Medium 500.

**Scale Ratio**: 1.25 (Major Third)

### Radius & Border

```
radius-sm:   8px
radius-md:   16px
radius-lg:   24px
radius-full: 9999px
border-width: 2px     // Chunky borders by default
```

**Special "Blob" Radius**: `rounded-tl-2xl rounded-tr-2xl rounded-br-2xl rounded-bl-none` (Speech bubble) or `rounded-t-full rounded-b-none` (Arch).

### Shadows & Effects

**The "Pop" Shadow (Hard Shadow)**:
```
box-shadow: 4px 4px 0px 0px #1E293B;
box-shadow-hover: 6px 6px 0px 0px #1E293B;
box-shadow-active: 2px 2px 0px 0px #1E293B;
```
No blur. Solid offset.

### Textures & Patterns
- **Dot Grid**: Background of small dots in strict formation.
- **Squiggles**: SVG paths as section dividers or underlining for headings.
- **Confetti**: Small SVG shapes (triangles, circles) absolutely positioned behind main content blocks.

---

## Component Stylings

### Buttons

**Primary Button ("The Candy Button")**:
```
- Bg: accent (#8B5CF6) Text: white, font-weight: 700 Radius: rounded-full Border: 2px solid #1E293B Shadow: 4px 4px #1E293B Hover: translate -2px shadow 6px Active: translate +2px shadow 2px Icon: ArrowRight in white circle
```

**Secondary**: `Bg transparent Text foreground Border 2px #1E293B rounded-full Hover bg-tertiary (#FBBF24)`

### Cards

**The "Sticker" Card**: `Bg white Border 2px #1E293B rounded-xl Shadow 8px #E2E8F0 or #F472B6 Hover Rotate -1deg Scale 1.02 Title Bold Outfit Icon floating half-in/half-out circle div`

### Inputs

`Bg white Border 2px #CBD5E1 rounded-lg Text foreground Shadow 4px transparent hidden Focus Border accent Shadow 4px accent Label Bold uppercase small tracking-wide`

---

## Layout Strategy

- Container `max-w-6xl`, `py-24` (96px), 12-col grouped 6/6 or 4/4/4
- Hero: Text left, Image right, massive yellow circle behind text, dotted pattern behind image, image blob mask
- Features: 3 grid connected by dashed SVG line, alternating Violet/Pink/Yellow headers
- Pricing: middle scaled 1.1, yellow star badge "MOST POPULAR" rotate 15deg

---

## Effects & Animation

**Feel**: Bouncy, Elastic, Fun. Hover `transition-all duration-300 ease-[cubic-bezier(0.34,1.56,0.64,1)]` (overshoot). Entrance pop Scale 0→1 with bounce. Marquee infinite logos. Wiggle `rotate 0→3→-3→0` on icons.

## Iconography

Lucide stroke 2.5px bold chunky round caps, often white inside colored circle, or dark foreground. Never floating alone. Enclosed in shapes.

## Responsive

Stack on mobile, reduce pop shadows 2px, hide complex floating shapes, keep buttons 48px+.

## Accessibility

AAA slate-800 on off-white, never color alone, prefers-reduced-motion disable bounce/wiggle, focus thick colored border + hard shadow.

</design-system>

---

## How to use this skill

- Load `design-template-playful-geometric` when task is playful / memphis / sticker.
- Signature: `#FFFDF5` + Violet #8B5CF6 + Pink #F472B6 + Amber #FBBF24 + Emerald + hard shadow 4px.

## Playful Geometric Checklist

- [ ] Palette `#FFFDF5`/`#1E293B` + `8B5CF6` primary + `F472B6`/`FBBF24`/`34D399` rotational confetti.
- [ ] Typography Outfit 700/800 + Plus Jakarta Sans 400/500, scale 1.25, `rounded-tl-2xl` blob variants.
- [ ] Effects hard shadow `4px 4px #1E293B` → `6px` hover / `2px` active, dot grid + squiggles + confetti.
- [ ] Buttons pill `rounded-full` `border-2` hard shadow candy style, cards sticker `rounded-xl` `hover:rotate-1 scale-1.02`.
