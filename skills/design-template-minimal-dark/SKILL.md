---
name: design-template-minimal-dark
description: "Minimalist Dark — deep slate #0A0A0F, amber #F59E0B glow, glass cards, Space Grotesk, atmospheric. Use when user wants minimal dark, dark minimal, atmospheric dark, slate + amber, premium dark."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-minimal-dark

> Minimalist Dark — Atmospheric Depth, not pure black. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-minimal-dark design-template-<nama>`.

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
# Design Style: Minimalist Dark

## Design Philosophy

### Core Principle

**Atmospheric Depth.** Minimalist Dark creates visual interest not through color saturation or complex patterns, but through carefully orchestrated layers of darkness. Multiple shades of slate and charcoal stack upon each other, with warm amber accents that glow like embers in the night. The design breathes—generous whitespace (or rather, "darkspace") gives every element room to exist.

### Visual Vibe

**Emotional Keywords**: Atmospheric, Sophisticated, Calm, Premium, Nocturnal, Refined, Spacious, Warm-cool contrast, Ethereal, Grounded

This is the visual language of premium dark mode apps (Linear, Raycast, Arc), high-end dev tools (Vercel, Railway), luxury tech at night.

### The DNA

1. Layered Slate #0A0A0F → #12121A → #1A1A24, not pure black
2. Warm Amber #F59E0B single accent, glowing embers
3. Ambient glow `0 0 20px rgba(245,158,11,0.4)` behind badges/buttons/orbs
4. Glass cards `rgba(26,26,36,0.6) backdrop-blur 8px` border 0.08
5. Space Grotesk display + Inter body + JetBrains Mono labels
6. Breathing room `py-24→40`, 3 dark tones visible
7. Subtle borders `rgba(255,255,255,0.08)` 1px

### Differentiation

| Aspect | Minimalist Modern | Minimalist Monochrome | Minimalist Dark |
| Mode | Light | Light | **Dark** |
| Background | Off-white | Pure white | Deep slate #0A0A0F |
| Accent | Blue gradients | None | Warm amber #F59E0B |
| Typography | Sans + serif | Serif | Geometric sans |
| Corners | Rounded lg/xl | Sharp 0px | Soft md/lg |
| Depth | Shadows+glows | Flat | Ambient glows + glass |
| Feel | Energetic | Editorial austere | Atmospheric calm |

---

## Design Token System

### Colors (Dark Slate + Amber)

```
background:       #0A0A0F
backgroundAlt:    #12121A
foreground:       #FAFAFA
muted:            #1A1A24
mutedForeground:  #71717A
accent:           #F59E0B
accentForeground: #0A0A0F
accentMuted:      rgba(245,158,11,0.15)
border:           rgba(255,255,255,0.08)
borderHover:      rgba(255,255,255,0.15)
card:             rgba(26,26,36,0.6)
cardSolid:        #1A1A24
ring:             #F59E0B
```

### Typography
- Display: `"Space Grotesk"` geometric
- Body: `"Inter"`
- Mono: `"JetBrains Mono"`
- Scale xs→7xl (12px→96px), tracking-tight headlines, tracking-wide labels

### Radius
```
sm 6px md 8px lg 12px xl 16px 2xl 24px full 9999px
```

### Shadows & Glows
```
sm 0 1px 2px rgba(0,0,0,0.3)
md 0 4px 6px rgba(0,0,0,0.3)
glowSm 0 0 20px rgba(245,158,11,0.15) glowMd 0 0 40px 0.2 glowLg 0 0 60px 0.25 borderGlow 0 0 0 1px 0.3 + 0 0 20px 0.15
```

### Textures
- Noise 0.02, radial `rgba(245,158,11,0.03)`, grid `rgba(255,255,255,0.02) 40px`

---

## Component Stylings

### Buttons
- Primary: `#F59E0B` text `#0A0A0F` `rounded-lg` `px-6 py-3 h-11` `font-medium` hover `brightness-110 shadow-[0_0_20px_rgba(245,158,11,0.4)]` active `scale-0.98`
- Secondary: transparent `border-white/15` hover `bg-white/5`
- Ghost: transparent hover `bg-white/5`

### Cards (Glass)
- `rgba(26,26,36,0.6) backdrop-blur 8px border white/0.08 rounded-lg lg 12px` hover `border white/15 bg 0.8 scale-1.02 shadow md` highlighted `border amber/0.2 + glow`

### Inputs
- `rgba(26,26,36,0.6) blur 8px border white/0.08 rounded-lg h-11 text #FAFAFA placeholder #71717A` focus `border-amber/50 ring amber/20 glow`

---

## Layout

- Container `max-w-6xl px-6→12`, section `py-24→40`, gap `6/8`, layered dark tones, ambient orbs `blur 100-150px` amber 0.02-0.04 fixed, noise 0.015

---

## Effects & Animation

- Motion smooth subtle 200-300ms ease-out, cards 300ms, ambient orbs blur, no bounce. Pulse dot, FAQ accordion, scale 1.02/0.98, glows.

## Iconography

`strokeWidth 1.5 size 20`, zinc-400 → amber-500 on accent, subtle support.

## Responsive

Scale `text-4xl→7xl` hero, `lg:grid-cols-2` stack, glow orbs smaller mobile, `h-11/12` 44px min, `hidden md:flex` nav, hover→active on touch, glass maintained.

## Accessibility

- Contrast 18.4:1 AAA / 4.9:1 AA, focus `ring-accent ring-offset-background`, labels.

## Bold Choices (Non-Negotiable)

1. 3 dark tones visible, 2. Warm amber #F59E0B only, 3. Glows behind badges/buttons/orbs 100-150px blur, 4. Glass 0.6 + blur 8px, 5. Spacious `py-24→40`, 6. Borders 8% opacity, 7. Space Grotesk + Inter + Mono, 8. Ambient orbs + noise, 9. Scale 1.02/0.98, FAQ smooth.

## Full Original Prompt Reference

*Full design-system verbatim as provided by user (phosphor palette section etc.) preserved in repo for fidelity. This distilled version keeps tokens + components + motion identical but compressed for token efficiency. Agent should treat distilled spec as source of truth — if detail needed, refer to verbose spec in git history.*

</design-system>

---

## How to use this skill

- Load `design-template-minimal-dark` when task is minimal dark / slate + amber atmospheric.
- Signature: `#0A0A0F` + Amber `#F59E0B` + Glass + Space Grotesk + ambient glow + darkspace.

## Minimal Dark Checklist

- [ ] Palette `#0A0A0F`/`#12121A`/`#1A1A24` + `#F59E0B` amber + `#FAFAFA` + borders `white/0.08`.
- [ ] Typography Space Grotesk + Inter + Mono, `tracking-tight` headlines.
- [ ] Glass `rgba(26,26,36,0.6) blur 8px` + glow orbs `100-150px`.
- [ ] Spacious `py-24→40`, subtle borders, no harsh lines.
