---
name: design-template-maximalism
description: "Maximalism Dopamine — void #0D0D1A + magenta #FF3AF2 + cyan #00F5D4 + yellow #FFE600 + orange #FF6B35 + purple #7B2FFF, 5 accents, triple text-shadow, hard 8px. Use when user wants maximalism, dopamine, more is more, hyperpop, y2k, lisa frank."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-maximalism

> Maximalism / Dopamine — MORE IS MORE sensory overload joyful. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-maximalism design-template-<nama>`.

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
# Design Style: Maximalism / Dopamine

## Design Philosophy

**Core Principle**: MORE IS MORE. Rejects minimal restraint for sensory overload visual abundance unapologetic excess. Every pixel spark joy. Empty space wasted. Patterns clash colors scream elements overlap chaotic intention.

**Emotional Target**: Euphoric playful overwhelming Y2K Gen-Z hyperpop. Lisa Frank fever Nickelodeon slime hyperpop album fireworks Skittles.

**Guiding Question**: "Is this visually overwhelming in a joyful way?" If no add more.

---

## Design Token System (The DNA)

### Color Palette (Dark Mode Foundation)

**Base**: Background `#0D0D1A` Deep cosmic purple-black void, Foreground `#FFFFFF` Pure white 19.5:1 AAA, Muted `#2D1B4E` Dark purple semi-transparent containers, Border Base `#FF3AF2` Hot magenta default.

**The Five Accents** (critical always 5):
```
1. Accent Magenta #FF3AF2 electric energy
2. Secondary Cyan #00F5D4 digital glow
3. Tertiary Yellow #FFE600 screaming attention
4. Quaternary Orange #FF6B35 warmth chaos
5. Quinary Purple #7B2FFF mystical depth
```

**Color Usage Rules**: Section Rotation each major section cycles 5 accents `index%5` systematically, Repeated Elements grid rotate modulo 5, No Matching borders clash background magenta→yellow/cyan, Contrast White `#FFFFFF` on dark `19.5:1 AAA`, Accent Text only decorative not body.

### Typography System

**Font Stack**: Headings `"Outfit" bold geometric 700-900` or `"Unbounded"`, Body `"DM Sans" 400-700`, Display/Accent `"Bangers"/"Bungee"` comic energy sparingly.

**Type Scale Aggressive**: Hero `7xl→9xl 72-128px MASSIVE`, Section `5xl→7xl 48-72px Bold`, Sub `2xl→3xl 24-30px`, Body `lg→xl 18-20px` Larger than typical, Small `sm→base 14-16px`. Weight Headlines 800-900 body 400-500 labels 700 bold, Letter Spacing headlines `tracking-tight/tighter` labels `tracking-widest` body normal, Line Height headlines `none/tight 0.9-1.1` body `relaxed 1.625`, Transform UPPERCASE headlines labels buttons Normal body, Mixed Weights varying within headline.

**Text Shadow System** (CRITICAL Always Use):
```
Single: 2px 2px 0px #7B2FFF
Double: 2px 2px #7B2FFF, 4px 4px #FF3AF2
Triple: 2px #7B2FFF, 4px #FF3AF2, 6px #00F5D4
Mega: 4px #7B2FFF, 8px #FF3AF2, 12px #00F5D4
```
2px increments rotate accents Headlines triple mega Sub double Card title single double

**Gradient Text**: 20-30% headlines `linear-gradient 90deg #FF3AF2, #00F5D4, #FFE600, #FF3AF2` 200-300% animate gradient shift `background-clip: text` transparent.

### Border & Radius System

**Border Widths** Go bold: Standard `border-4 4px` most common Heavy `border-8 8px` dividers/featured Subtle `border-2 2px` inner only.

**Border Styles** Mix deliberate: Solid Default most containers cards, Dashed 30% borders variety `dashed`, Dotted rare small decorative, Double occasional special containers `double`, Critical Within single section use 2-3 different styles intentionally.

**Border Radius Values**:
```
Buttons: rounded-full 9999px pill
Cards: rounded-3xl 24px generous curves
Containers: rounded-2xl 16px moderate curves
Sharp Accent: rounded-none 0px use sparingly contrast
Mixed: different radii different corners asymmetry
```

**Border Color Strategy**: Primary Accent color clash background Never neutral muted Technique If background accent-1 border accent-2/3.

### Shadow & Glow System (Multi-Layered)

**Glow Shadows** (Colored soft luminous):
```
Base Glow: 0 0 20px rgba(255,58,242,0.5), 0 0 40px rgba(0,245,212,0.3)
Large Glow: 0 0 40px rgba(255,58,242,0.6), 0 0 80px rgba(255,230,0,0.4), 0 0 120px rgba(123,47,255,0.3)
```
Buttons icons featured Hover increase opacity 0.1-0.2 spread 50% Combine 2-3 colors richer.

**Hard Shadows** (Offset flat stacked):
```
Double Stack: 8px 8px 0 #FFE600, 16px 16px 0 #FF3AF2
Triple Stack: 12px 12px 0 #00F5D4, 24px 24px 0 #FF3AF2, 36px 36px 0 #FFE600
```
Each layer doubles offset 8→16→24 or 12→24→36 Colors rotate different accents per layer Use Cards containers prominent buttons Hover Increase offsets 2-4px simulate lift

**Shadow Mixing**: Combine glow + hard on hero `0 0 30px rgba(255,58,242,0.6), 8px 8px 0 #FFE600, 16px 16px 0 #FF3AF2`

*Full verbose patterns in git history.*

</design-system>

---

## How to use this skill

- Load `design-template-maximalism` when task is maximalism / dopamine.
- Signature: `#0D0D1A` + 5 accents magenta/cyan/yellow/orange/purple + triple text-shadow + `border-4` clash.

## Maximalism Checklist

- [ ] Palette `#0D0D1A` + `#FFFFFF` 19.5:1 + 5 accents #FF3AF2/#00F5D4/#FFE600/#FF6B35/#7B2FFF rotate `index%5`, clash borders never match.
- [ ] Typography Outfit/Unbounded 900 `7xl→9xl` + triple `2px 2px` shadow rotating accents + gradient shift 4s, UPPERCASE headlines.
- [ ] Borders `4/8px` solid/dashed/dotted mixed `rounded-3xl/2xl/full` varied.
- [ ] Shadows glow + hard stacked 8→16→32, patterns dots `20px` stripes `45deg 10px` checker `40px` mesh radial 2-4 overlaps opacity 0.05-0.3 at least 2 layers per section.
- [ ] Bold 10: floating shapes 5-10 per section, massive `12-20rem` typography, pattern-on-pattern 2-3 layers, systematic color rotation, clashing borders `4px`, multi-layer shadows, asymmetric `translate-y-8` rotate `1-2deg`, mixed border styles, emoji `6xl` bounce, gradient text 20-30% headlines, animations float `6s` pulse glow `2s` gradient-shift `4s` spin `20s` wiggle `1s` bounce `2s`.
