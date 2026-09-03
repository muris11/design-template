---
name: design-template-vaporwave
description: "Vaporwave Outrun — void #090014, magenta #FF00FF, cyan #00FFFF, orange #FF9900, Orbitron, scanlines, perspective grid, glitch. Use when user wants vaporwave, outrun, retro futurism, sunset gradient, 80s, synthwave, CRT."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-vaporwave

> Vaporwave / Outrun — synthetic digital nostalgia neon. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-vaporwave design-template-<nama>`.

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
# Vaporwave / Outrun Design System

## 1. Design Philosophy

**"Digital Nostalgia meets Neon Future — synthetic reality drenched in retro-futuristic excess."**

Bold celebration of 80s retro-futurism, vaporwave, early computer graphics. Synthetic digital dimension where neon pierces infinite grids, CRT scanlines distort reality, every interaction feels like commanding vintage terminal from 2088.

**Core Aesthetic DNA**:
- Visual Language: High-contrast maximalism unapologetic neon saturation. Dense layered effects depth overlapping gradients, glows, scanlines, perspective distortions.
- Emotional Tone: Nostalgic yet futuristic. Retro (80s arcade, VHS, Windows UIs) + forward-looking (cyberpunk cityscapes, holographic). Dreamy synthetic surreal.
- Design Pillars: Infinite Grid perspective wireframe receding horizon (outrun highway), Neon Glow Supremacy Hot magenta #FF00FF cyan #00FFFF orange #FF9900 with drop shadows, CRT Scanlines + RGB chromatic aberration, Terminal/Command-Line `>` Share Tech Mono, Geometric Transformation skew/rotate perspective, Gradient Mania multi-stop sunset yellow→orange→pink→purple.

**Interaction Philosophy**: Hover theatrical: buttons un-skew explode glow scale invert, icons rotate, cards lift.

**Anti-Patterns**: NOT flat, NOT minimalist, NOT corporate, NOT muted — maximal saturated.

## 2. Design Token System (The DNA)

### Colors (Dark Mode Only)

*   Background Void `#090014` purple tint infinite.
*   Foreground Chrome `#E0E0E0` silver-gray.
*   Card Glass Panels `rgba(26,16,60,0.8)` `#1a103c` deep purple semi-transparent backdrop-blur.
*   Primary Hot Magenta `#FF00FF` hero CTAs highlights avatars feature icons accent borders THE hero.
*   Secondary Electric Cyan `#00FFFF` links focus rings secondary borders hover, complements magenta.
*   Tertiary Sunset Orange `#FF9900` sparse special highlights sun gradients attention.
*   Border Default `#2D1B4E` muted dark purple, Active `#00FFFF`/`#FF00FF`.

**Gradient Combinations**:
- Sunset `linear-gradient(to right, #FF9900, #FF00FF, #00FFFF)` signature text fills
- Glow `linear-gradient(to bottom, #FF9900, #FF00FF)` floating sun
- Accent Bar `linear-gradient(to right, #FF00FF, #00FFFF)` top borders

### Typography

*   Headings `"Orbitron" sans-serif 400/500/700/900` geometric wide futuristic all-caps extreme weights 900 tight tracking.
*   Body/UI/Code `"Share Tech Mono" monospace 400` technical terminal fixed-width uppercase UI normal case body tracking wide.
*   Type Scale Hero `5xl→9xl 80-128px` multi-line drama, Section `3xl→6xl` bold/black, Card `2xl` cyan glow `drop-shadow-[0_0_5px_rgba(0,255,255,0.8)]`, Body `lg→xl 18-20px` generous, UI `sm→lg all-caps tracking-wider/widest`.
*   Text Effects Glow `drop-shadow-[0_0_10px_rgba(255,255,255,0.5)]`, Gradient `bg-gradient-to-r from-[#FF9900] via-[#FF00FF] to-[#00FFFF] bg-clip-text`.

### Radius & Borders

**Border Philosophy**: Sharp geometric neon light tubes non-subtle. Radius `rounded-none 0px` primary. Angular. Occasional `rounded-full` dots/circles only. Width `border-2 2px` standard Heavier `border-4` for emphasis/containers. Colors Default `#2D1B4E` Interactive Hover `#00FFFF`/`#FF00FF` Top Accent Bars Gradient or solid cyan `border-t-2`.

### Shadows & Effects (The Glow)

Box Shadows Neon Glow: Magenta `shadow-[0_0_10px_#FF00FF]`/`20px`, Cyan `shadow-[0_0_20px_rgba(0,255,255,0.2)]` containers `50px`, Text Shadows see Typography, Hover amplification 2-3x base glow.

### Textures & Background Patterns

Pattern Philosophy Void never empty Layers grids scanlines dots gradients dimensional depth.

*   Perspective Grid Floor: `linear-gradient(trans 95%, #FF00FF 95%) 40px` `perspective(500px) rotateX(60deg) translateY(-100px) scale(2) mask linear to bottom` iconic receding.
*   Floating Sun: `h-[600px] w-[600px] blur-[100px] bg-gradient-to-b from-[#FF9900] to-[#FF00FF] opacity-20`
*   Global Scanlines Overlay: `linear-gradient(rgba(18,16,20,0) 50%, rgba(0,0,0,0.25) 50%) 100% 4px` fixed `z-50` CRT.
*   RGB Chromatic `linear-gradient 90deg rgba(255,0,0,0.06), rgba(0,255,0,0.02), rgba(0,0,255,0.06))`
*   Dot Patterns `radial-gradient(#FF00FF 1px, transparent 1px) 20px` sections.
*   Gradient Overlays Images Duotone `from-[#FF00FF] to-[#00FFFF] opacity-20 mix-blend-overlay`.

## 3. Component Stylings

### Buttons

Primary `variant=primary`: `-skew-x-12 border-2 #00FFFF bg-transparent text #00FFFF rounded-none uppercase tracking-wider font-mono hover:skew-0 hover:bg #00FFFF text black shadow 20px`. Inner counter-skewed span `skew-x-12`.

Secondary `border-2 #FF00FF bg #FF00FF text white hover:skew-0 scale-105 opacity-80`
Outline `border-2 #FF00FF bg transparent text #FF00FF hover bg #FF00FF white`
Ghost `text #E0E0E0 hover bg rgba(0,255,255,0.1) text #00FFFF`

Sizes `sm h-9 default h-12 lg h-14 icon h-10 w-10`

### Cards / Containers

Standard: `border border-[#FF00FF]/30 border-t-2 border-t-[#00FFFF] bg-[#1a103c]/80 backdrop-blur-md p-6 Title font-heading semibold 2xl text #00FFFF glow drop-shadow hover, Description font-mono #E0E0E0/70 sm`.

Terminal Window (Product Detail): `border-2 #00FFFF bg-black/80 shadow 20px rgba(0,255,255,0.2) Title bar bg #00FFFF/10 border-b #00FFFF px-4 py-2 dots h-3 w-3 #FF00FF/#00FFFF/#FF9900`

File Explorer (Benefits): `border-2 #E0E0E0/20 bg-[#1a103c]/90 backdrop-blur Title bar bg #E0E0E0/10 border-b-2 #E0E0E0/20 Status bar border-t-2 #E0E0E0/20 bg #090014 text #E0E0E0/50 xs`

### Inputs

Terminal-Style: `border-b-2 #FF00FF bg-black text #00FFFF font-mono lg px-3 py-2 placeholder #FF00FF/50 focus border #00FFFF shadow 15px #00FFFF outline-none`.

## 4. Non-Generic "Bold" Choices (The "Wow" Factor)

1. Aggressive Skewing `-skew-x-12` un-skew hover kinetic morphing 2. Global CRT Scanlines fixed viewport horizontal + RGB 3. Perspective Grid Backgrounds receding 4. Gradient Text Fills multi-stop clipped 5. Rotating Icon Containers `rotate-45` diamond spin `rotate-90` hover 6. Dual-Border Patterns cyan top + pink sides layered neon tubes 7. Terminal/Window Chrome vintage OS title bars file explorer 8. Massive Blurred Sun `600px blur 100px` gradient orb depth 9. IRC-Style `<username>` angle bracket testimonials 10. Alternating Timeline central checkpoint line 11. Glowing Hover Amplification 2-3x glow color inversions.

## 5. Animation & Motion

Snappy mechanical retro-digital `duration-200 ease-linear` Fast unnatural digital No organic easing. Hover Un-skew fill invert explode glow, Cards `-translate-y-2`, Icons rotate 45° or scale, Links underline glow. Continuous `animate-pulse` trust, Terminal cursor blink. Transform origins perspective `top/bottom center` `transition-all`.

## 6. Layout Strategy & Spacing

Container `max-w-7xl` / `6xl` pricing `4xl` FAQ/CTA `5xl` hero Section `py-20 sm:py-32` Component `gap-8/12` Inner `p-6/8` Margins `mb-8→20` Grids Features `1 md:3` Stats `1 md:2 lg:4` Blog `1 md:3` Benefits `1 md:2 lg:3` Pricing `1 md:3` Z-Index back grid `z-0` floating sun, Content `z-10`, Scanline `z-50`.

## 7. Responsive Strategy

Mobile-first `sm md lg`. Mobile: Typography `5xl→8xl` reduce 1-2 sizes `py-32→20 mb-20→12` Stack single col Buttons full-width Stack vertically Timeline left-aligned offset Borders maintain neon Glow slightly reduce intensity Grid keep perspective. Tablet 2 col mid sizes Full menu. Key vaporwave MUST survive mobile — neon glows borders grids non-negotiable `h-12 h-14 44px`.

## Full Verbose Spec Preserved in Git History

</design-system>

---

## How to use this skill

- Load `design-template-vaporwave` when task is vaporwave / outrun / sunset synth.
- Signature: `#090014` + Magenta #FF00FF + Cyan #00FFFF + sunset gradient + CRT + perspective grid.

## Vaporwave Checklist

- [ ] Palette void `#090014` + magenta/cyan/orange neons, gradients sunset `FF9900→FF00FF→00FFFF`.
- [ ] Typography Orbitron 900 `5xl→9xl` uppercase + Share Tech Mono, glow `drop-shadow`.
- [ ] Effects scanlines `4px` + perspective grid `40px 500px rotateX60` + sun `600px blur 100px`.
- [ ] Components skew `-12` buttons chamfer + terminal windows + top cyan border.
