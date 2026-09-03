---
name: design-template-web3
description: "Web3 Bitcoin DeFi — void #030304, Bitcoin orange #F7931A→#EA580C, gold #FFD600, Space Grotesk + glass, orbital rings, grid. Use when user wants web3, bitcoin, defi, crypto, blockchain, glass morphism, luminescent."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-web3

> Web3 Bitcoin DeFi — digital gold luminescent. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-web3 design-template-<nama>`.

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
# Design Philosophy: The "Bitcoin DeFi" Aesthetic

This style embodies the visual DNA of Bitcoin and decentralized finance—a sophisticated fusion of precision engineering, cryptographic trust, and digital gold. It is **not generic dark mode**; it is a deep cosmic void where data structures glow with the warmth of Bitcoin orange and the brilliance of digital gold.

## Core Design Principles

1.  **Luminescent Energy**: Light emanates from interactive elements themselves. Bitcoin orange glows, golden highlights shimmer, and data points pulse with life against the true void background. Shadows are colored (orange/gold tints), not just black.

2.  **Mathematical Precision**: Everything follows strict geometric rules. Ultra-thin 1px borders define boundaries, monospace fonts display data with technical accuracy, and grids provide the underlying structure of the blockchain aesthetic.

3.  **Layered Depth**: Create three-dimensional space through transparency stacking (glass morphism), colored glow shadows, and backdrop blur effects. Elements float in Z-space without heavy skeuomorphism—it's digital depth, not physical.

4.  **Textured Void**: Backgrounds are never flat. Subtle grid patterns (representing blockchain networks), radial gradient blurs (representing energy fields), and noise textures bring the void to life. The darkness breathes.

5.  **Trust Through Design**: High contrast, clear hierarchy, and technical precision communicate security and reliability. The aesthetic says "your assets are safe here."

The vibe is **Secure, Technical, and Valuable**. This is digital gold—it should feel premium, cutting-edge, and engineered to perfection. Think Bitcoin mining rigs humming in the darkness, glowing with orange heat.

# Design Token System

## Colors (Dark Mode Only)
This palette uses a "True Void" foundation with "Bitcoin Fire" energy—the warmth of Bitcoin orange and the brilliance of digital gold.

*   **Background**: `#030304` (True Void) - The deepest space where all begins
*   **Surface**: `#0F1115` (Dark Matter) - Elevated surfaces, cards, and panels
*   **Foreground**: `#FFFFFF` (Pure Light) - Primary text, maximum contrast
*   **Muted**: `#94A3B8` (Stardust) - Secondary text, descriptions, metadata
*   **Border**: `#1E293B` (Dim Boundary) - Subtle borders at rest (often at 10-20% opacity when using white)
*   **Primary Accent**: `#F7931A` (Bitcoin Orange) - The iconic color of decentralization. Primary CTAs, links, active states, and trust indicators
*   **Secondary Accent**: `#EA580C` (Burnt Orange) - A deeper, warmer orange for gradients, secondary elements, and visual depth
*   **Tertiary Accent**: `#FFD600` (Digital Gold) - The color of value. Used in gradients with Bitcoin Orange, highlights, and success states

**Gradient Formula**: The signature look is `linear-gradient(to right, #EA580C, #F7931A)` or `linear-gradient(to right, #F7931A, #FFD600)` for text and buttons.

## Typography
The type system balances technical precision with modern geometric forms.

*   **Headings**: `Space Grotesk` (Google Font) - A geometric grotesque with quirky technical character
    *   Weights: 400 (Regular), 500 (Medium), 600 (Semibold), 700 (Bold)
    *   Usage: All headings (h1-h6), section titles, card titles
    *   Apply `font-heading` class

*   **Body**: `Inter` (Google Font) - Highly legible sans-serif optimized for screens
    *   Weights: 400 (Regular), 500 (Medium), 600 (Semibold)
    *   Usage: Body copy, descriptions, buttons
    *   Apply `font-body` class

*   **Mono/Data**: `JetBrains Mono` (Google Font) - Technical monospace for precision
    *   Weights: 400 (Regular), 500 (Medium)
    *   Usage: Stats, prices, badges, technical labels, navigation links
    *   Apply `font-mono` class

*   **Scale Philosophy**: Dramatic contrast between display and body. Heroes are massive (`text-4xl` → `md:text-7xl`), body is comfortable (`text-base` or `text-lg`). Mobile-first scaling prevents overwhelming small screens.

*   **Leading & Tracking**: Tight leading on headings (`leading-tight`), relaxed on body (`leading-relaxed`). Uppercase mono text gets generous tracking (`tracking-wider`, `tracking-widest`).

## Radius & Borders
Geometric precision with soft curves for approachability.

*   **Radius Tokens**:
    *   Cards/Containers: `rounded-2xl` (16px) or `rounded-xl` (12px)
    *   Buttons: `rounded-full` (pill shape)
    *   Inputs: `rounded-lg` (8px) or bottom-border only for minimalism
    *   Small elements (badges, icons): `rounded-lg` or `rounded-full`

*   **Border Philosophy**: Ultra-thin `1px` borders create delicate boundaries without visual weight
    *   Default state: `border border-white/10` (barely visible structure)
    *   Hover state: `border-[#F7931A]/50` (orange accent, 50% opacity)
    *   Active/Focus: `border-[#F7931A]` (full intensity)

## Shadows & Effects (The Glow)
The signature of this style is **colored luminescence**—shadows and glows in Bitcoin orange and gold tints.

*   **Orange Glow** (Primary): `shadow-[0_0_20px_-5px_rgba(234,88,12,0.5)]` or `shadow-[0_0_30px_-5px_rgba(247,147,26,0.6)]`
*   **Gold Glow** (Accent): `shadow-[0_0_20px_rgba(255,214,0,0.3)]`
*   **Subtle Card Elevation**: `shadow-[0_0_50px_-10px_rgba(247,147,26,0.1)]`
*   **Glass Morphism**: `backdrop-blur-lg` + `bg-white/5` or `bg-black/40`
*   **Radial Blur Backgrounds**: `bg-[#F7931A] opacity-10 blur-[120px]` absolutely positioned

## Textures & Patterns
*   **Grid Pattern** (Signature): 50px grid with `rgba(30,41,59,0.5)` lines + vignette mask `radial-gradient(circle at center, black 40%, transparent 100%)`
*   **Cubes Pattern**: `transparenttextures.com/patterns/cubes.png` opacity-5
*   **Radial Gradient Blurs**: `blur-[120px]` soft orbs at 5-10% opacity

# Component Stylings

## Buttons
- Primary: `bg-gradient-to-r from-[#EA580C] to-[#F7931A]` white bold uppercase `tracking-wider` pill `rounded-full` glow `shadow-[0_0_20px_-5px_rgba(234,88,12,0.5)]` hover `scale-105` intensified glow
- Outline: `border-2 border-white/20` transparent white → hover `border-white` + `bg-white/10`
- Ghost: transparent → hover `bg-white/10` + `text-[#F7931A]`

## Cards (The "Block" Concept)
- Standard: `bg-[#0F1115]` `border border-white/10` `rounded-2xl` `p-8` hover `-translate-y-1` + `border-[#F7931A]/50` + orange glow
- Glass: `bg-black/40` `backdrop-blur-sm` `border-white/10`
- Pricing highlighted: `scale-105` `border-[#F7931A]` + `shadow-[0_0_40px_-10px_rgba(247,147,26,0.15)]`

## Inputs
- `bg-black/50` `border-b-2 border-white/20` `h-12` `px-4` `text-white` placeholder `white/30` focus `border-[#F7931A]` + glow `shadow-[0_10px_20px_-10px_rgba(247,147,26,0.3)]`

## Icons
- lucide `text-[#F7931A]` or Gold, containers `bg-[#EA580C]/20 border-[#EA580C]/50 rounded-lg p-3` + glow

# Non-Generic "Bold" Choices
1. Gradient text `from-[#F7931A] to-[#FFD600] bg-clip-text` on hero final words
2. Spinning orbital rings `spin 10s` + reverse 15s + bouncing stat cards + `animate-ping`
3. Corner accents orange on How It Works cards
4. Background icon watermarks `opacity-20 → 100` on hover
5. Timeline as blockchain vertical gradient line + circular nodes
6. Asymmetric pricing `scale-105` vs `opacity-80`
7. Glass + grid pattern depth
8. Colored shadows only (orange/gold)

# Layout & Spacing
- `max-w-7xl` `py-24` `gap-8/12` no hard dividers, alternating `bg-[#030304]`↔`bg-[#0F1115]`

# Animation & Motion
- `animate-float 8s ease-in-out`, `spin 10s/15s`, `animate-bounce 3/4s`, `animate-ping`, `duration-200/300`

# Responsive Strategy
- Mobile-first `text-4xl→7xl`, grids 1→2→3, 44px targets, hero `h-[300px] md:h-[450px]`, stack pricing

# Accessibility
- Contrast AAA 21:1, focus `ring-[#F7931A]`, semantic HTML, reduced-motion

</design-system>

---

## How to use this skill

- Load `design-template-web3` when task is web3 / Bitcoin DeFi.
- Signature: Void `#030304` + Orange `#F7931A→#EA580C` + Gold `#FFD600` + glass.

## Web3 Checklist

- [ ] Palette `#030304`/`#0F1115` + `#F7931A`/`#EA580C`/`#FFD600` + white `#FFFFFF` + grid `#1E293B`. Colored glows only.
- [ ] Typography Space Grotesk headings + Inter body + JetBrains Mono data, gradient text `F7931A→FFD600`.
- [ ] Radius `2xl` cards + `full` pills, borders `1px white/10` → hover `F7931A/50`.
- [ ] Effects orange/gold glow + `backdrop-blur-lg` + radial blur 120px + grid 50px vignette.
- [ ] Bold 8: gradient text + orbital rings + corner accents + watermarks + timeline blockchain + scale pricing + glass+grid + colored shadows.
