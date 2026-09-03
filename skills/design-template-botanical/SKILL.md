---
name: design-template-botanical
description: "Botanical Organic Serif — alabaster #F9F8F4 + forest #2D3A31 + sage #8C9A84 + terracotta #C27B66, Playfair Display arch 200px, paper grain, staggered. Use when user wants botanical, organic, sage, terracotta, nature, garden, wellness, artisan."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-botanical

> Botanical / Organic Serif — digital ode to nature, sun-warmed artisanship. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-botanical design-template-<nama>`.

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
# Design Style: Botanical / Organic Serif

## 1. Design Philosophy

This style is a **digital ode to nature**—it breathes, flows, and grounds itself in organic beauty. Soft, sophisticated, intentional, rejecting rigid hyper-digital sharpness for warmth, tactility, natural imperfection.

**Core Essence**: Botanical garden, ceramics studio, editorial elegance. Whispers not shouts. Hand-touched, sun-warmed, naturally crafted.

**Fundamental Principles**:

*   **Vibe**: Peaceful, curated, artisanal, high-end wellness, sustainable luxury, botanical elegance
*   **Visual DNA**:
    *   **Organic Softness**: Hard angles rare. Every corner rounded, every shape flows like water-smoothed stones. 200px arch on images iconic.
    *   **Typographic Elegance**: Playfair Display high-contrast strokes commanding grace. Italics handwritten personal. Headlines `5xl→8xl` airy.
    *   **Earthbound Palette**: Forest floors, clay pottery, sage gardens, terracotta tiles. Muted sophisticated grounded.
    *   **Tactile Texture**: Paper grain overlay mandatory `opacity-[0.015]` fractal noise fixed `z-50`—without it loses soul.
    *   **Breathing Space**: `py-32` `gap-8/16` sacred.
    *   **Intentional Movement**: Slow fluid 500-700ms `ease-out`, plants swaying.
    *   **Staggered Rhythm**: Every second card `translate-y-12` breaking grid creating organic flow. Images rotate subtly.

## 2. Design Token System

### Colors (Light Mode - Earthy & Muted)
*   **Background**: `#F9F8F4` Warm Alabaster / Rice Paper — not stark white.
*   **Foreground**: `#2D3A31` Deep Forest Green — softer than black.
*   **Primary/Accent**: `#8C9A84` Sage Green — buttons, highlights, icons.
*   **Secondary/Muted**: `#DCCFC2` Soft Clay / Mushroom — card backgrounds, secondary buttons.
*   **Border**: `#E6E2DA` Stone — very subtle low contrast.
*   **Interactive**: `#C27B66` Terracotta — hover CTA pops.

### Typography
*   **Headings**: **"Playfair Display"**. High contrast transitional serif classic modern. Weight 600/700 italicize key words.
*   **Body**: **"Source Sans 3"**. Clean humanist sans 400/500.
*   **Scaling**: Large airy grand.

### Radius & Shapes
*   **Radius**: Highly rounded. Standard Card `rounded-3xl 24px`, Buttons `rounded-full` Pill, Images `rounded-t-full` Arch or `rounded-[40px]`.
*   **Border**: Thin delicate `1px` solid.

### Shadows & Effects
*   Very soft diffused no harsh dark drops. Default `0 4px 6px -1px rgba(45,58,49,0.05)` Medium `0 10px 15px -3px 0.05` Large `0 20px 40px -10px 0.05` Extra Large `0 25px 50px -12px 0.15`
*   **Paper Grain Texture** (CRITICAL): Fixed `opacity-[0.015]` SVG fractal noise `baseFrequency 0.9 numOctaves 4`.
*   **Blur**: `backdrop-blur-sm` on hero quote card.

## 3. Component Stylings

### Buttons
*   Primary: Pill `rounded-full` Background Deep Forest `#2D3A31` White text Hover lightens or shifts Terracotta. Uppercase `tracking-widest` `text-sm`.
*   Secondary: Transparent Sage border `1px` Text Sage.
*   Hover `bg-opacity-90` `duration-300` etc.

### Cards (Features, Pricing)
*   Background White `#FFFFFF` or Soft Clay `#F2F0EB`. Border none or subtle Stone `#E6E2DA`. Shape `rounded-3xl`. Hover `-translate-y-1` bloom soft shadow.

### Inputs
*   Underlined only `Border-bottom` or pill light `#F2F0EB`. Focus soft Sage Green `ring-[#8C9A84]`.

## 4. Non-Generic "Bold" Choices
*   Arch Imagery `rounded-t-full 200px` or `clip-path`, Overlapping Typography big serif overlapping images/shapes, Decorative Lines fine 1px SVG vines, Italic Emphasis *Italic* Playfair within bold headline.

## 5. Layout Strategy & Spacing
*   Container `max-w-7xl` airiness. Whitespace `gap-12/16` `py-24/32` Grid break `translate-y-12` staggered natural.

## 6. Icons (Lucide React)
*   Thin `stroke-width 1.5` Deep Forest or Sage floating or pale circles.

## 7. Animation & Micro-Interactions
*   Slow graceful fluid 300 fast 500 standard 700-1000 dramatic Images `scale-105 duration-700` luxurious, Cards `-translate-y-1/2`, Buttons subtle, Blog lift + arrow `translate-x-1`, Accordion `max-h-0→48` + opacity, Mobile menu slide, Scroll fade up.

## 8. Responsive Strategy
*   Mobile-first: Hero `aspect-[3/4] mobile → square fixed md`? Actually hero image aspect handling, Grids `1→md:3`, Stats `2→4`, Blog `1→3`, Pricing `1→3`, Typography `text-8xl→5xl` mobile, Spacing `py-32→16`, Staggered only `md:` Touch 44px.

*Full verbose spec preserved in git history — distilled keeps tokens identical.*

</design-system>

---

## How to use this skill

- Load `design-template-botanical` when task is botanical / organic / sage.
- Signature: `#F9F8F4` + Sage #8C9A84 + Playfair arch 200px + paper grain.

## Botanical Checklist

- [ ] Palette `#F9F8F4` / `#2D3A31` / `#8C9A84` / `#DCCFC2` / Terracotta #C27B66.
- [ ] Typography Playfair 600/700 italic emphasis + Source Sans 3, grain overlay mandatory.
- [ ] Radius `3xl/40px/full` organic, `rounded-t-full` arch images.
- [ ] Textures paper grain `0.015` + staggered `translate-y-12` + slow 500-700ms.
