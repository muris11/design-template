---
name: design-template-retro
description: "Retro 90s Nostalgia — win95 #C0C0C0, navy #000080, #0000FF blue link, bevel outset/inset, tiled pattern, rainbow text, marquee. Use when user wants retro, 90s, geocities, windows 95, vapor nostalgic, under construction, hit counter."
allowed-tools: Read Write Edit Glob Grep
---
# design-template-retro

> Retro / 90s Nostalgia — ugly-cool Windows 95. One template in `design-template` family. Copy this folder to create next template: `Copy-Item design-template-retro design-template-<nama>`.

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
# Retro / 90s Nostalgia Design System

## Design Philosophy

**Core Principles**: Raw unfiltered early web ugly-cool beveled buttons system fonts garish colors animated. Deliberately anti-modern rejecting minimalism max visual impact nostalgic authenticity. Every pixel 1997 Windows 95 800x600.

**Vibe**: Playful chaotic nostalgic loud GeoCities Under Construction hit counters guestbooks optimistic experimental.

**Historical Context**: 1995-1999 Windows 95/98 monitors 800x600 limited CSS severe constraints distinctive language faithfully recreating.

---

## Design Token System (The DNA)

### Colors (Light Mode Only) Windows 95 system

| Token | Value | Usage | Notes |
| background | #C0C0C0 | Primary page | Win95 button face gray |
| foreground | #000000 | Pure black text | Max contrast no grays |
| muted | #808080 | Secondary metadata | 50% gray 128 |
| accent | #0000FF | Hyperlinks unvisited | Pure blue max sat |
| secondary | #FF0000 | Hot red emphasis | Pure red max |
| tertiary | #FFFF00 | Bright yellow highlights | Pure yellow badges |
| success | #00FF00 | Lime green | Pure green max |
| successDark | #00AA00 | Darker green buttons | Readable |
| border | #000000 | Pure black borders | Outer |
| borderLight | #FFFFFF | White 3D highlight | Top/left bevel |
| borderDark | #808080 | Gray 3D shadow | Bottom/right bevel |
| titleBar | #000080 | Win title navy | Pure dark blue Navy |
| titleBarGradientEnd | #1084D0 | Title bar gradient | Win98 active gradient |
| panelYellow | #FFFFCC | Light yellow panels | Notepad/help |
| visitedLink | #800080 | Visited | Purple/Maroon |
| hoverLink | #FF0000 | Link hover | Red |

Color Relationships All max sat pure RGB at least one channel 0/255 No gradual grays only `#000 #808080 #C0C0C0 #FFF`, Links progression Blue→Purple visited→Red hover.

### Typography

**Font Stacks** (System fonts 1995-1999):
- Primary Body: `"MS Sans Serif", "Segoe UI", Tahoma, Geneva, Verdana, sans-serif`
- Headings: `"Arial Black", Impact, Haettenschweiler, sans-serif` heavy bold only
- Monospace: `"Courier New", Courier, monospace` dates stats counters code-like
- Playful ultra-sparingly: `"Comic Sans MS", cursive` fun decorative if needed

**Type Scale**: H1 Hero 48-96px `3xl→6xl` always UPPERCASE or Title Case Arial Black/Impact, H2 Section 32-48px `2xl→4xl` often UPPERCASE Arial Black, H3 20-24px `lg→xl` bold, Body 14-16px default, Small/Meta 12px `xs` often monospace dates metadata, Labels 10-12px UPPERCASE sometimes monospace.

**Typographic Patterns**: Headings BOLD or BLACK no thin/light, Letter-spacing `tracking-tight→wide` not expanded, Line-height Dense 1.2-1.4 headings 1.5-1.6 body, Text shadows 3D `2px 2px 0 #808080` hard no blur.

### Radius & Borders

**Border Radius**: `0px` EVERYWHERE No exceptions 90s didn't have radius.

**Border Widths**: Standard `2px` most Emphasis `4px` dividers highlighted Minimum `1px` subtle inner rare.

**3D Bevel Effect** (THE SIGNATURE) Windows 95 4-value border-color + box-shadow depth.

**Outset Raised** Pop out:
```css
border: 2px solid; border-color: #ffffff #808080 #808080 #ffffff; /* Top Right Bottom Left */
box-shadow: inset -1px -1px 0 #404040, inset 1px 1px 0 #dfdfdf;
```
Top/left white Bottom/right gray Inner darker #404040 lighter #dfdfdf.

**Outset Enhanced Deeper**:
```css
border: 2px solid; border-color: #ffffff #808080 #808080 #ffffff;
box-shadow: inset -2px -2px 0 #808080, inset 2px 2px 0 #fff, inset -4px -4px 0 #404040, inset 4px 4px 0 #dfdfdf;
```

**Inset Sunken** Pressed in Reversed `border-color: #808080 #ffffff #ffffff #808080; box-shadow: inset 1px 1px 0 #404040, inset -1px -1px 0 #dfdfdf;` Top/left gray Bottom/right white.

**Active/Pressed**: Outset becomes inset AND `translate(1px,1px)`: `border-color: #808080 #fff #fff #808080; box-shadow: inset 1px 1px 0 #404040, inset -1px -1px 0 #dfdfdf; transform: translate(1px,1px);`

Tailwind Arbitrary `[border-color:#fff_#808080_#808080_#fff]` `[box-shadow:inset_-1px_-1px_0_#404040,inset_1px_1px_0_#dfdfdf]`

### Textures & Patterns (MANDATORY) Background must NOT flat critical authenticity.

**90s Tiled Pattern** Primary: `bg #c0c0c0` `linear-gradient 45deg #b8b8b8 25%` 4 patterns 4px `background-size 4px 4px position 0 0, 0 2px, 2px -2px, -2px 0` diagonal crosshatch texture.

**Construction Warning Stripes** Emphasis: `repeating-linear-gradient 45deg #ffff00 #ffff00 10px #000000 10px #000000 20px` Exactly 10px yellow 10px black 45°.

**Horizontal Rule HR Groove**: `border none height 4px bg linear to bottom #808080 0% #808080 50% #ffffff 50% #ffffff 100%` etched divider.

---

## Component Styling Principles

### Buttons
Visual 2px 4-value outset color pattern Background subtle gradient or solid per variant Text Bold UPPERCASE `tracking-wide` centered Padding 8px vertical 16px horiz NO radius NO soft shadows.

State Default Outset slightly lighter hover Hover lightens 1-2 shades maintain outset Active Inset reversed translate 1px Focus Dotted 2px black outline 2px offset Windows 95 focus ring Transition NONE or instant `transition-none` or 50ms max no smooth easing.

Variants Default/Ghost `#C0C0C0` black outset, Accent/Primary `#0000FF` white blue-tinted bevel, Danger `#FF0000` white red-tinted bevel, Success `#00AA00` white green-tinted bevel, Outline White black outset. Bevel Tinting Colored buttons tint bevel matching: Blue `border-color: #5555ff #000080 #000080 #5555ff` etc. Example Tailwind `border-2 bg-[#c0c0c0] text-black [border-color:#fff_#808080_#808080_#fff] [box-shadow:inset_-1px_-1px_0_#404040,inset_1px_1px_0_#dfdfdf] hover:bg-[#d0d0d0] active:[border-color:#808080_#fff_#fff_#808080] active:translate-[1px] focus-visible:outline-dotted focus-visible:outline-2 focus-visible:outline-black focus-visible:outline-offset-2`.

### Cards/Containers
Panel/Card Structure Container 2px outset bevel `#C0C0C0` Title bar Gradient `to right #000080, #1084d0` white bold 4-8px padding Content area Inset bevel sunken white or `#FFFFCC` yellow. Window-Style Card Distinctive Outer outset gray Title navy gradient white bold Content inset white padding 16px Alternating Row Backgrounds Even `#FFFFFF` Odd `#E8E8E8` classic spreadsheet Borders Between Cells `border-right-2 border-bottom-2 #808080` visible grid.

### Form Inputs
Input Fields Border 2px inset sunken White Black 14-16px Padding 4-8px Focus Dotted 2px black outline 2px offset Disabled `#C0C0C0` 50% opacity Placeholder `#808080` Select same Dropdowns inset Checkboxes rare text indicators squares.

### Links (Hyperlinks) Iconic 90s

States Unvisited `#0000FF` blue underlined always Visited `#800080` purple Hover `#FF0000` red Active while clicking `#FF0000` red Rules ALWAYS underlined never remove instant no transitions No background hover No additional styling Example `text-[#0000ff] underline hover:text-[#ff0000] visited:text-[#800080]`.

### Icons
Styling Stroke 2px thick bold lines Color match accent section blue red green Size 24px `h-6 w-6` standard 32px features NO rounded soft shapes Consider adding 2px black borders around icon containers. Icon Containers Box solid bright color `#000080 #008080 #00AA00` Icon White Box Outset or flat with borders.

---

## Layout Principles

### Page Structure

Maximum Width `max-w-5xl 1024px` mimics 800x600 monitor content area browser chrome

Spacing Base 8px Element padding 16px Element margins 8-16px tighter density Section padding 64px vertical `py-16` 16px horiz `px-4`

Section Dividers Thick `border-b-4 border-[#808080]` OR groove HR effect between major sections.

Grid Layouts Even though modern Grid/Flex make LOOK like tables: Visible cell borders `border-2` or `border-r-2/b-2` Alternating row backgrounds Equal column widths where possible Dense compact spacing

### Responsive Strategy

Desktop 768px+ Full table-like side-by-side Multi-column 2-4 columns Visible complex borders Tablet 640-768 Reduce to 2 cols max Maintain all visual bevels borders Stack complex tables if needed Mobile <640 Single column KEEP beveled effects essential style Marquee continues Reduce font sizes slightly keep bold weights Horizontal scrolling for complex tables acceptable authentic! Important aesthetic more important than perfect responsiveness slightly janky authentic era.

---

## The "Bold Factor" (MANDATORY ELEMENTS)

1. Marquee Scrolling Text `react-fast-marquee` speed 30-60 no gradient fade multiple spans different colors 2. Animated Rainbow Text `rainbow 4s linear infinite` cycling bright colors hero `0% #ff0000 17% #ff8000 33% #ffff00 50% #00ff00 67% #0080ff 83% #8000ff 100% #ff0000` linear no smoothing 3. Beveled Everything 3D outset/inset NON-NEGOTIABLE 4. Under Construction Energy Blinking NEW badges `animate-pulse` or CSS blink step-end Pulsing call-to-action Pulse Glow `0%,100% scale1 box-shadow 0 0 0 0 rgba(255,0,0,0.7) 50% scale1.05 box-shadow 0 0 10px 2px rgba(255,0,0,0.5)` 1.5s ease-in-out infinite 5. Horizontal Rules HR groove 3D etched 6. Hit Counter aesthetic Stats black/navy bg green monospace `#00FF00` beveled inset frame `Visitors: 0001234 | Since 1995` 7. Table-Like Visual Layouts visible cell borders alternating row backgrounds grid precision 8. Title Bar Windows navy-to-blue gradient white bold title inset content below 9. Decorative Color Squares grid bright squares red green blue yellow magenta cyan beveled edges pure decorative 90s excess 10. Construction Stripe Background yellow/black diagonal section like final CTA.

## Animation & Motion

Snappy immediate digital No organic easing. Timing Instant `transition-none duration-0` Color cycling `linear` Badges `ease-in-out` Button press `transition-none` or max 50ms Durations Button instant/50ms Hover 75ms or instant Rainbow 3-5s Pulse 1-2s Marquee 40-60px/s Key Rainbow 4s linear infinite pulse-glow 1.5s ease-in-out blink 1s step-end marquee continuous pauseOnHover usability Reduced Motion respect `prefers-reduced-motion` Stop rainbow fallback single bright Stop marquee static/slower Stop pulsing static bright.

## Accessibility

Contrast 7.5:1 AAA 8.6:1 AAA Palette naturally excellent, Focus 2px dotted black outline 2px offset high visibility never remove, Keyboard All interactive keyboard Tab order visual Button press Enter/Space active, Screen Readers Marquee aria-live polite Decorative aria-hidden Color squares no alt Semantic HTML table-like appearance, Motion reduced alternatives `@media (prefers-reduced-motion: reduce) .text-rainbow {animation:none; color:#ff0000}` etc.

## Anti-Patterns (What to AVOID)

Visual NO border-radius Not even 1px Zero Always NO soft drop shadows Only inset bevels NO gradients except Title bar navy→blue Background patterns stripes tiles Subtle button backgrounds NO semi-transparent overlays Colors always opaque except white/80 secondary on dark NO thin fonts Everything bold/black NO subtle grays Only `#000 #808080 #C0C0C0 #FFF #E8E8E8` NO smooth easing Use linear instant NO removing link underlines Always visible NO modern minimalist spacing Dense not airy NO attempt modernize Embrace cheese Interaction DON'T hover scale except 1.05 pulse badges DON'T fade transitions instant/linear DON'T make marquee essential decorative supplemental DON'T override selection color DO use #000080 bg white text DON'T floating action buttons modern patterns Content DON'T placeholder not era no lorem ipsum DON'T reference modern tech decorative generic/90s DON'T be subtle LOUD PROUD.

## Implementation Notes

Tailwind Arbitrary `border-[2px] [border-color:#fff_#808080_#808080_#fff] [box-shadow:inset_-1px_-1px_0_#404040,inset_1px_1px_0_#dfdfdf] bg-[#c0c0c0] text-[#0000ff]` Use underscores spaces. Custom CSS Required `@keyframes rainbow pulse-glow blink` `.hr-groove .bg-90s-tile .bg-construction` Dependencies `react-fast-marquee` Essential authentic scrolling Create CSS variables complex box-shadow reusability Color Layering Base Tiled #C0C0C0 Surface White/gray panels Accent Navy title bars colored feature boxes Foreground Black text colored icons Highlights Yellow badges red NEW tags rainbow text.

## Signature Visual Checklist

- [ ] ≥1 marquee scrolling colorful text
- [ ] Rainbow animated text hero/major heading
- [ ] All buttons 3D outset bevels proper border-color syntax
- [ ] ≥1 card Windows 95 title bar gradient
- [ ] Tiled background pattern visible main body
- [ ] Hyperlinks blue/underlined turn red hover
- [ ] ≥1 section alternating row backgrounds
- [ ] Horizontal groove rule divider between major sections
- [ ] Hit counter style stats monospace green
- [ ] One NEW!/HOT! badge pulse animation
- [ ] Construction stripe background ≥1 section
- [ ] All interactive dotted focus outlines
- [ ] Active buttons pressed state inset+translate
- [ ] Icons 2px stroke width
- [ ] Zero border-radius anywhere

## The Secret Sauce

Commitment authenticity over modernization Temptation clean professional Resist ugliness IS beauty clashing colors dense layouts aggressive animations features Someone lived 1997 transported back jarring next modern websites That contrast IS point Embrace cheese Celebrate chaos Welcome 1997.

*Full verbose spec in git history.*

</design-system>

---

## How to use this skill

- Load `design-template-retro` when task is retro 90s windows95.
- Signature: `#C0C0C0` + bevel outset `[border-color:#fff_#808080]` + `0px` + rainbow marquee.

## Retro Checklist

- [ ] Palette `#C0C0C0` + black #000 + blue #0000FF/#000080 navy + red/yellow/green pure RGB max sat.
- [ ] Typography `MS Sans Serif` + `Arial Black` UPPERCASE + `Courier New` mono stats, bold/black only.
- [ ] Borders `0px` everywhere bevel outset/inset `2px [border-color:#fff_#808080...]` + inset shadow.
- [ ] Textures tiled `4px` crosshatch + construction stripes `10px yellow/black` + groove HR `4px`.
- [ ] Components buttons outset → active inset `translate 1px`, cards title bar gradient navy→blue + inset white, links blue→purple→red underlined.
- [ ] Bold 10: marquee + rainbow `4s linear` + beveled everything + NEW pulse + HR groove + hit counter green mono + table grid + title bar windows + color squares + construction stripe.
