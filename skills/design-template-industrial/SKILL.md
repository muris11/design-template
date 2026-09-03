---
name: design-template-industrial
description: "Industrial Skeuomorphism — chassis #e0e5ec, charcoal #2d3436, safety orange #ff4757, Inter + JetBrains Mono, neumorphic dual shadows, screws, vents. Use when user wants industrial, skeuomorphism, neumorphism, mechanical, Dieter Rams, Teenage Engineering."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-industrial

> Industrial Skeuomorphism — tactile mechanical realism. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-industrial design-template-<nama>`.

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
# Design Style: Industrial Skeuomorphism

## 1. Design Philosophy

This style transcends simple skeuomorphism into **Industrial Realism** — tactile precision, mechanical reliability, soul of physical objects. Offers solid grounded permanent vs ephemeral flat digital.

**Core DNA**:
- **Physicality Through Light**: Every element 3D top-left 45° light consistent highlight top/left shadow bottom/right dual shadows.
- **Mechanical Authenticity**: Interactions mimic physics buttons depress `translate-y-2` shadow inversion, cards elevate, icons rotate, spring bounce.
- **Manufacturing Details Matter**: Corner screws radial gradients at 12px, ventilation slots pill `inset`, LED indicators pulsing glow `0 0 10px rgba(255,71,87,0.6)`, scanlines, push-pin shadows, hanging holes pricing — signature.
- **Material Honesty**: Matte ABS plastic chassis `#e0e5ec`, brushed aluminum, powder-coated steel safety-orange controls `#ff4757`, noise texture `mix-blend-overlay` 20-30%, carbon fibre `transparenttextures.com`.
- **Vibe**: Spacecraft control panel, Braun 1980s synthesizer, Teenage Engineering OP-1 — functional organized precise cool. Dieter Rams max clarity min ornament, Teenage playful modular, Timeless 1985↔2035.
- **Physics Engine**: Consistent top-left 45°, Material Conservation slide not appear, Elevation -1 Recessed (inputs/screens inset) 0 Chassis `e0e5ec` +1 Panels cards dual shadows +2 Floating Controls buttons enhanced glow, Interaction Active inset Hover elevate spring `cubic-bezier(0.175,0.885,0.32,1.275)`.

## 2. Design Token System (The DNA)

### Colors (Industrial Palette) Strictly Light Mode

- Background Chassis `#e0e5ec` cool mid-tone industrial grey Level 0.
- Foreground Panel `#f0f2f5` lighter raised.
- Muted Recessed `#d1d9e6` darker sunken input bezels grooves.
- Text Primary `#2d3436` charcoal high contrast softer than pure black.
- Text Muted `#4a5568` slate grey AA.
- Accent Safety Orange `#ff4757` Braun Red emergency stop — only interactive triggers alerts LEDs, Foreground `#ffffff`.
- Border Shadow `#babecc` darker half, Border Light Highlight `#ffffff` brighter half, Border Dark `#a3b1c6` prominent dividers.
- Dark Accent Surfaces charcoal `#2d3436/#2c3e50` text `#ffffff/#e0e5ec/#a8b2d1` accent same orange.

### Typography

**Font Pairing**: Primary `Inter 400/500/600/700/800` humanist neutral functional. Technical `JetBrains Mono 400/500` for numeric stats pricing dates labels badges small uppercase metadata inputs.

Hierarchy Hero `5xl-7xl 3-4.5rem 800 tight -0.03em drop-shadow 0 1px 1px #fff`, Section `3xl-4xl 700 tight`, Body Base-lg 400-500 normal 1.6-1.75 max 60-65 chars, Labels xs-sm 700 uppercase wide 0.05-0.08em monospace stamped, Buttons uppercase wide 0.05em 700 xs-base.

### Radius & Depth

**Border Radius**: `sm 4px` mechanical `md 8px` controls `lg 16px` panels `xl 24px` hero `2xl 30px+` `full 9999px` circles LED step.

Curves soft injection-molded not machined.

**Neumorphic Shadow System** (Core Signature):
- Card Base Lift: `8px 8px 16px #babecc, -8px -8px 16px #ffffff`
- Floating High: `12px 12px 24px #babecc, -12px -12px 24px #ffffff, inset 1px 1px 0 rgba(255,255,255,0.5)`
- Pressed Active: `inset 6px 6px 12px #babecc, inset -6px -6px 12px #ffffff`
- Recessed Inputs: `inset 4px 4px 8px #babecc, inset -4px -4px 8px #ffffff`
- Sharp Mechanical: `4px 4px 8px rgba(0,0,0,0.15), -1px -1px 1px rgba(255,255,255,0.8)`
- Glow LED: `0 0 10px 2px rgba(255,71,87,0.6)` green `rgba(34,197,94,1)` online.

Layered Hover additional shadows `transition 300ms cubic-bezier`.

### Textures & Patterns

Noise Overlay SVG fractal noise 20-30% `mix-blend-overlay` matte plastic micro-texture entire page. Carbon Fiber `carbon-fibre.png` 10-20% tech sections `multiply`, Scanlines `linear-gradient(rgba(18,16,16,0)50%, rgba(0,0,0,0.25)50%) 100% 4px` on screens, Grid `linear-gradient(#636e72 1px) 40px 0.1` blueprint, Radial Gradients top-left white/transparent lighting.

## 3. Component Stylings

### Buttons ("Physical Keys") Tactile 3D pressability

Structure Primary Accent `#ff4757` white uppercase wide track `rgba(255,255,255,0.2)` rim `4px 4px 8px rgba(166,50,60,0.4), -4px -4px 8px rgba(255,100,110,0.4)` Secondary Chassis `#e0e5ec` dark text base lift hover accent Ghost Flat muted hover muted + recessed.

Interaction Hover brightness+110 Active `translate-y-2` shadow inversion `inset 6px 6px 12px` border vanish `150ms`, Focus `ring-2 ring-[var(--ring)] ring-offset-2`, Sizing min 48px mobile generous.

### Cards ("Bolted Modules") Physical panels bolted

Construction `shadow-card` neumorphic dual `lg 16px` `Chassis` optional `elevated floating`, Manufacturing Details Corner Screws radial gradients at 12px, Vent Slots `h-6 w-1 rounded-full bg-muted shadow inset` 3 `gap-1`, Hover lift `-translate-y-1` `shadow-floating` `300ms ease-out` group icon rotate/scale.

### Inputs ("Data Slots") Recessed wells machined

`shadow-recessed` inset `border-none` Chassis bg `rounded md 8px` `JetBrains Mono` `h-14` `px-6 24px` placeholder `50%`, Focus glow `shadow-recessed,0 0 0 2px accent`, Disabled `50%`.

## 4. Layout Strategy

Container `72rem 1152px` `px-6→12` `space-y-24 96px` Grid `gap-6/8` alignment mounted invisible grid Asymmetry 60/40 hero stacked mobile alternate left/right testimonials `±1deg` rotation `order-1/2`.

## 5. Non-Genericness (Signature Elements)

Hero Device 3D mockup CSS — outer bezel 4px rounded carbon texture, inner screen black inset scanline, hardware buttons side LED, abstract dashboard glowing spinning loaders status bars hover scale.

LED Status small 8-12px `animate-pulse glow 0 0 10px` green/red/yellow Navbar hero badge footer device monospace label `SYSTEM OPERATIONAL`.

Connectors Pipes How It Works `h-3 w-full rounded-full bg-d1d9e6 inset` `hidden md:block`.

Masking Tape Stickers skewed yellow `rgba(255,230,0,0.3) backdrop-blur-sm` blog dates testimonials, Push Pins red `top center highlight shine` testimonials, Hanging Holes pricing circular `inset` punched metal, Screws Vent Slots never omit DNA.

Grayscale→Color `grayscale group-hover:grayscale-0 duration-500`.

## 6. Effects & Animation

Mechanical spring bounce `cubic-bezier(0.175,0.885,0.32,1.275)` Fast 150-200 Smooth 300 Image scale 500, Framer Motion staggered slideUp `opacity+y` mechanical `[0.175,0.885,0.32,1.275]`, Micro Button Press `2px` Card `-1` Icon `110 + rotate-12` Image grayscale LED pulse 2s Radar `4s conic-gradient spin`.

## 7. Iconography & Icon Integration

lucide-react Stroke 1.5 thin 1-2px 20-24px UI 28-32px feature 16-18px inline `accent` or text match. Integration Recessed Housing `h-14 w-14 rounded-full bg-background shadow-floating text-accent 28px`, Inline `Zap h-4 text-accent`, Nav `Twitter h-5 hover text-accent`, LED solid fill glow `12-16px`.

## 8. Responsive Strategy

Physical metaphor persists all breakpoints no generic mobile. Breakpoints `md768 lg1024 xl1280` Navigation hamburger drawer neumorphic, Hero side-by-side→stacked device aspect `aspect-square mobile aspect-video desktop`, Grids 3→1 4→2 Pricing 3→1 Testimonials 3→1 Images aspect maintain, Touch 48px `w-full sm:w-auto` Buttons full mobile Typography `7xl→5xl` Body `lg` Spacing `96→64` Card `32→24` Hidden Pipes hidden.

Performance external textures small cached `transform/opacity` GPU CSS-only shadows.

*Full verbose spec in git history.*

</design-system>

---

## How to use this skill

- Load `design-template-industrial` when task is industrial / skeuomorphic / neumorphic.
- Signature: `#e0e5ec` chassis + orange `#ff4757` + dual neumorphic shadows + screws + vents.

## Industrial Checklist

- [ ] Palette `#e0e5ec`/`#f0f2f5`/`#d1d9e6` + `#ff4757` only interactive, noise + carbon patterns.
- [ ] Typography Inter 800 `5xl-7xl` + JetBrains Mono labels uppercase wide, `0 1px #fff` emboss.
- [ ] Shadows dual neumorphic card/floating/pressed/recessed + glow LED, no flat drop shadows.
- [ ] Components: buttons physical keys press inversion, cards bolted screws + vents, inputs recessed inset.
