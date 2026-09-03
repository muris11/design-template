---
name: design-template-claymorphism
description: "Claymorphism — candy clay #F4F1FA, violet #7C3AED, Nunito, 60px super-rounded, 4-layer clay shadows, squish. Use when user wants claymorphism, clay, vinyl toy, soft 3d, inflated, bouncy, marshmallow, high-fidelity clay."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-claymorphism

> High-Fidelity Claymorphism — digital clay tactile. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-claymorphism design-template-<nama>`.

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
# High-Fidelity Claymorphism Design System

## Design Philosophy

**Core Concept: Digital Clay**
This design system is not merely a "soft UI"—it is a high-fidelity simulation of a tangible, physical world constructed from **premium digital clay**. Every element should evoke holding a high-end, matte-finish vinyl toy or soft silicone object. It rejects flatness in favor of volume, weight, and tactility.

**The "High-Fidelity" Difference**: Unlike early neumorphism (extruded plastic) or basic claymorphism (flat vector), **High-Fidelity Claymorphism** uses 4-layer shadow stacks. Objects feel dense, substantial—not hollow.

*   **Materiality**: Soft-touch matte silicone, marshmallow-like foam, premium injection-molded plastic.
*   **Lighting**: Soft diffused overhead top-left, deep ambient occlusion below, gentle specular highlights on ridges.
*   **Shadow Architecture**: 4-layer stacks — outer drop + top-left highlight + inner colored bounce + inner rim light. Active uses inset.

**The Sensory Vibe**:
*   **Playful & Optimistic**: Candy store colors (violet #7C3AED, pink #DB2777, blue #0EA5E9, emerald #10B981, amber #F59E0B) + bouncy organic motion.
*   **Tactile & Responsive**: Squish `scale-[0.92]` + `shadow-clayPressed` on press, lift `-translate-y-2` on hover.
*   **Friendly & Safe**: Zero sharp corners — `rounded-[20px]` min up to `rounded-[60px]`, subconsciously safe.
*   **Premium Craft**: Consistent radii, precise shadow layering, harmonious colors.

**The "Clay" Physics Engine**:
1. **Convexity**: Bulge OUT with `shadow-clayButton`/`shadow-clayCard` — light top-left, soft colored shadow below.
2. **Concavity**: Pressed IN with `shadow-clayPressed` — inset top, lip light bottom (inputs, active).
3. **Buoyancy**: Zero-gravity high air resistance — blobs drift 8-12s `translateY` + rotate, cards hover.
4. **Micro-Physics**: Hover lift `hover:-translate-y-1→2` + shadow enhance, active compress `scale-0.92`.

---

## Design Token System

### Colors (The "Candy Shop" Palette)

**Background**: `#F4F1FA` (Very pale cool lavender-white) — never pure white.

**Foreground**: `#332F3A` (Soft Charcoal) — softer than black, WCAG AA.
**Muted**: `#635F69` (Dark Lavender-Gray) — body text minimum lighter bound.

**Accents**: `#7C3AED` Vivid Violet (primary), `#DB2777` Hot Pink, `#0EA5E9` Sky Blue, `#10B981` Emerald, `#F59E0B` Amber.

**Gradient**: Primary buttons `from-[#A78BFA] to-[#7C3AED]`, icon orbs `from-*-400 to-*-600` pastel→saturated, hero text `from-clay-foreground 20%, to-clay-accent 60%`, blobs `opacity-10 blur-3xl`.

### Typography

**Headings**: **Nunito** 700/800/900 rounded terminals. Body: **DM Sans** 400/500/700.

**Hierarchy**:
- Hero: `text-5xl→8xl` Black 900 `tracking-tight` `leading-[1.1]` Nunito
- Section: `text-3xl→5xl` ExtraBold/Black Nunito
- Card: `text-xl→3xl` Bold-ExtraBold Nunito
- Body: `text-base→lg` Medium `leading-relaxed` DM Sans
- Small: `text-sm→xs` Medium/Bold tracking-wide

**Best Practices**: Pair Nunito + DM Sans, `font-black` for impact, `leading-relaxed` body, `max-w-2xl/3xl` 60-75 chars.

### Shapes & Radii

**The "Super-Rounded" Rule** (Absolute Values Only):
- Large Containers/Hero: `rounded-[48px]→[60px]`
- Standard Cards: `rounded-[32px]`
- Medium (Benefits/Blog): `rounded-[24px]`
- Buttons & Inputs: `rounded-[20px]` / `rounded-2xl`
- Icon Containers: `rounded-2xl` / `rounded-full`
- Stat Orbs: `rounded-full`

Never `rounded-md/sm` — too sharp.

### Shadows (The Engine of Clay)

**1. Deep Clay (Surface)**:
```
30px 30px 60px #cdc6d9, -30px -30px 60px #ffffff,
inset 10px 10px 20px rgba(139,92,246,0.05), inset -10px -10px 20px rgba(255,255,255,0.8)
```
**2. Clay Card (Floating)**: `16px 16px 32px rgba(160,150,180,0.2), -10px -10px 24px rgba(255,255,255,0.9), inset 6px 6px 12px rgba(139,92,246,0.03), inset -6px -6px 12px rgba(255,255,255,1)`
**3. Clay Button (Convex)**: `12px 12px 24px rgba(139,92,246,0.3), -8px -8px 16px rgba(255,255,255,0.4), inset 4px 4px 8px rgba(255,255,255,0.4), inset -4px -4px 8px rgba(0,0,0,0.1)`
**4. Clay Pressed (Recessed)**: `inset 10px 10px 20px #d9d4e3, inset -10px -10px 20px #ffffff`

---

## Component Architecture

### 1. The Universal Card
*   Base: `relative overflow-hidden rounded-[32px] bg-clay-cardBg p-8 shadow-clayCard backdrop-blur-xl`
*   Interactive: `shadow-clayCard` → `hover:-translate-y-2 hover:shadow-[enhanced]` `duration-500`
*   Structure: Outer wrapper + Inner `relative z-10 flex h-full flex-col` for peeking panels `-bottom-8 -left-8 -right-8`
*   Variants: Glass `bg-white/60→80`, Solid `bg-white`, Hero `md:col-span-2 md:row-span-2`

### 2. The Clay Button
*   Base: `rounded-[20px] h-14 (lg h-16) inline-flex font-bold tracking-wide duration-200`
*   Variants: Primary `from-[#A78BFA] to-[#7C3AED] text-white shadow-clayButton`, Secondary `bg-white`, Outline `border-2 border-clay-accent/20`, Ghost `hover:bg-clay-accent/10`
*   Interactive: `hover:-translate-y-1` + shadow enhance, `active:scale-[0.92] active:shadow-clayPressed`, `focus:ring-4 ring-clay-accent/30`

### 3. The Recessed Input
*   `rounded-2xl h-16 flex w-full border-0 bg-[#EFEBF5] px-6 py-4 text-lg shadow-clayPressed`, Focus `focus:bg-white focus:ring-4 focus:ring-clay-accent/20`, placeholder `text-clay-muted`

### 4. Floating 3D Blobs
*   Container `pointer-events-none fixed inset-0 overflow-hidden -z-10`, Blobs `absolute h-[60vh] w-[60vh] rounded-full blur-3xl bg-[color]/10` positioned ` -top-[10%] -left-[10%]` animated `clay-blob`/`clay-blob-alt` delay 2000/4000.

---

## Animation System

**clay-float** 8s `translateY 0→-20px rotate 0→2deg`, **clay-float-delayed** 10s ` -15px -2deg`, **clay-float-slow** 12s `-30px 5deg`, **clay-breathe** 6s `scale 1→1.02` on stat orbs.

Hover Lift: Cards `-translate-y-2` 8px + shadow, Benefits ` -1`, Testimonials `-2`, Blog `-3`, Buttons `-1`, Active Press `scale-0.92` + `shadow-clayPressed` 200ms, Scale orbs `110`, pricing `105`, hero `1.02`, delays 2000/4000.

**Reduced Motion**: `@media (prefers-reduced-motion: reduce)` disable all.

---

## Layout Patterns

Masonry/Bento `col-span-2 row-span-2` `hover:scale-[1.02]`; Split 50/50 Product/Benefits with Abstract 3D Composition; Overlapping `-top-6 -right-6` badges, `absolute opacity-10 text-9xl` textures.

---

## Responsive Strategy

Mobile-first progressive. Typography `text-5xl→8xl` hero `text-3xl→5xl` section, Navigation `h-16 rounded-[32px] px-4 → h-20 rounded-[40px] px-8` hide non-essentials, Hero stack `flex-col→sm:flex-row`, Stats `grid-cols-2→4`, Features Bento single→2→3, Benefits split stacked→`lg:grid-cols-2`, Pricing stacked→3, Cards `p-6→8`, Buttons `w-full→auto` 44px min, Decorative `hidden lg:block`, Shadows full retain.

## Dos and Don'ts

DO squish `0.92` + pressed, vary radii `48→32→24`, glass-clay `bg-white/60 backdrop-blur`, 4-layer stacks, Nunito headings, vibrant gradients. DON'T light gray `<#635F69`, sharp corners, flat bg, gradient text `<5xl`, small buttons `<h-11`, skip hover lift.

---

## Implementation Checklist
- [ ] Canvas `#F4F1FA` + Blobs 4-layer shadows Nunito Black + DM Sans `rounded-[32px]→[60px]` Gradient purple `20px` squish.

</design-system>

---

## How to use this skill

- Load `design-template-claymorphism` when task is clay / vinyl toy / marshmallow.
- Signature: `#F4F1FA` + Violet #7C3AED + Nunito + `rounded-[60px]` + 4-layer clay shadows + squish/breathe.

## Claymorphism Checklist

- [ ] Palette `#F4F1FA` / `#332F3A` / `#635F69` + Vivid Violet #7C3AED + Pink/Blue/Emerald/Amber candy, no sharp white.
- [ ] Typography Nunito 900 `5xl→8xl` `tracking-tight` + DM Sans body, DM Sans.
- [ ] Radius super-rounded `48→60px` hero `32px` cards `20px` buttons `full` orbs, never md/sm.
- [ ] Shadows 4-layer clay stacks (Surface/Card/Button/Pressed), highlight top-left, inner bounce, no flat shadows.
- [ ] Components: buttons gradient `from-[#A78BFA] to-[#7C3AED]` `rounded-[20px] h-14` squish+pressed, cards `bg-white/60 blur-xl rounded-[32px] shadow-clayCard`, inputs `bg-[#EFEBF5] h-16 pressed` focus white+ring.
- [ ] Blobs `60vh blur-3xl /10` drift 8-12s + `scale 105`, staggered delays.
- [ ] Motion bouncy `cubic-bezier` + breathe 6s, lift `-translate-y-1/2` + press `0.92`.
