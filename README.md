<p align="center">
  <img src="images/cover.png" alt="design-template cover" width="100%" />
</p>

<h1 align="center">design-template</h1>

<p align="center">
  <strong>30+ Production-Grade Design Systems as Agent Skills</strong><br/>
  Pure tokens. Zero guesswork. Every skill is a complete <code>&lt;role&gt;</code> + <code>&lt;design-system&gt;</code> ready to drop into any codebase.
</p>

<p align="center">
  <a href="https://github.com/muris11/design-template"><img src="https://img.shields.io/github/stars/muris11/design-template?style=flat&label=Stars" alt="GitHub Stars" /></a>
  <a href="https://www.npmjs.com/package/muris11-design-template"><img src="https://img.shields.io/npm/v/muris11-design-template?label=npm&color=CB0000" alt="npm version" /></a>
  <a href="https://www.skills.sh/muris11/design-template"><img src="https://img.shields.io/badge/skills.sh-design--template-7C3AED" alt="skills.sh" /></a>
  <a href="https://github.com/muris11/design-template/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-green" alt="MIT License" /></a>
  <img src="https://img.shields.io/badge/skills-30%2B-0A0A0A" alt="30+ Skills" />
  <img src="https://img.shields.io/badge/Claude%20Code-Compatible-5E6AD2" alt="Claude Code" />
  <img src="https://img.shields.io/badge/OpenCode-Compatible-FF6B6B" alt="OpenCode" />
</p>

<p align="center">
  <a href="./README.id.md">🇮🇩 Bahasa Indonesia</a> · <a href="#installation">Installation</a> · <a href="#skill-catalog">Catalog</a> · <a href="#usage">Usage</a> · <a href="https://github.com/muris11/design-template/issues">Issues</a>
</p>

---

## What is `design-template`?

`design-template` is **not a component library**. It is a **collection of 30 design identities** packaged as **agent skills** (`SKILL.md`) for AI coding agents (Claude Code, OpenCode, Cursor, Windsurf, Copilot).

Each sub-skill is **self-contained**: one `<role>` (how the agent works) + one `<design-system>` (tokens, components, layout, motion, textures) + a **delivery checklist**.

```
design-template/
├── design-template.md            # core router — lists all templates
├── skills/
│   ├── design-template/          # CORE — router skill (list, picker)
│   ├── design-template-all/      # LOADER — load everything at once
│   ├── design-template-monochrome/    # Pure B&W editorial
│   ├── design-template-bauhaus/       # Primaries + hard shadows
│   ├── design-template-swiss-minimalist/ # Swiss grid law
│   ├── ... 27 more templates ...
│   └── design-template-retro/         # Windows 95 90s nostalgia
```

**Why skills, not npm components?**

| Old way (components) | New way (skills) |
|---|---|
| Install a library, fight its API | Agent *reads* the design DNA, writes code in *your* stack |
| Locked to React/Vue | Works with any stack: React, Next.js, Vue, Svelte, HTML, Tailwind, shadcn |
| Generic output | Deliberate, opinionated output — every token has a reason |

> **One command:** Agent loads `design-template-monochrome` → instantly knows `#000/#FFF only`, `Playfair Display`, `0px`, `inversion`, no shadows — and writes code that matches.

---

## Features

- **30 templates** — from Minimalist Monochrome to Vaporwave to Brutalist — each with 400-800 lines of *actionable* design-system spec
- **100% token fidelity** — every color, radius, shadow, grid, type scale is written as copy-pasteable Tailwind / CSS
- **Role + System + Checklist** — every skill forces the agent to audit your stack → ask scope → plan → code → verify via checklist
- **Stack-agnostic** — React, Next.js, Vue, Svelte, Astro, HTML — agent adapts to *your* patterns
- **Claude Code native** — auto-discovered via `.claude-plugin/plugin.json` (`skills: ["./skills/"]`)
- **skills.sh & npm ready** — install via `npx skills add`, `npm i`, or git clone
- **Copy-paste to create** — `Copy-Item design-template-monochrome design-template-mybrand` — done

---

## Skill Catalog — 30 Templates + 2 Utilities

> **How to pick:** Find your vibe → note the skill name → load it. The agent does the rest.

| # | Skill | Vibe & Keywords | Palette | Typography | Signature | Trigger Words | Since |
|---|-------|-----------------|---------|------------|-----------|---------------|-------|
| 0 | `design-template` | **CORE router** — lists all templates | — | — | Picker table | `design-template`, `list templates` | v1.0.0 |
| 0 | `design-template-all` | **LOADER** — load all 30 at once | — | — | One-shot loader | `design-template semua`, `all` | v1.0.0 |
| 1 | `design-template-monochrome` | **Minimalist Monochrome** — Austere Editorial Luxury, Vogue / Celine | `#FFFFFF` `#000000` only | `Playfair Display` serif hero `8xl→9xl`, `JetBrains Mono` labels | 0px everywhere, inversion, horizontal-line texture 1.5%, hero oversized type | `monochrome`, `black white`, `editorial`, `luxury`, `stark`, `Vogue`, `no accent` | v1.0.0 |
| 2 | `design-template-bauhaus` | **Bauhaus** — Constructivist, Modernist, 1920s Poster | `#F0F0F0` + `#D02020` `#1040C0` `#F0C020` + `#121212` | `Outfit` 400/500/700/900 | `border-4` `#121212`, `shadow-[8px]` hard, `rounded-none/full` binary | `bauhaus`, `constructivist`, `geometric`, `primary colors` | v1.0.1 |
| 3 | `design-template-modern-dark` | **Modern Dark (Linear)** — Deep Space Cinematic, Raycast / Linear | `#050506` `#020203` `#5E6AD2` `#EDEDEF` | `Inter` / `Geist Sans` `tracking-[-0.03em]` | 4-layer bg (radial + noise + blobs `150px` + grid 64px), mouse spotlight 300px, parallax | `modern dark`, `linear`, `vercel`, `raycast`, `ambient glow` | v1.0.2 |
| 4 | `design-template-newsprint` | **Newsprint** — Golden Age Journalism, NY Times | `#F9F9F7` paper `#111111` ink `#CC0000` red | `Playfair Display` + `Lora` + `Inter` + `JetBrains Mono` `9xl` `leading-[0.9]` | `0px` + collapsed `border-r/b` grids + `hard 4px` shadow + dot/line textures + drop caps + Vol.1 | `newsprint`, `newspaper`, `broadsheet`, `journal`, `press` | v1.0.3 |
| 5 | `design-template-saas` | **Minimalist Modern SaaS** — SaaS Agency Premium | `#FAFAFA` `#0F172A` `#0052FF→#4D7CFF` | `Calistoga` + `Inter` + `JetBrains Mono` | Gradient `#0052FF` signature, inverted slate sections, floating cards 5s, pulsing dot, `rounded-xl/2xl` | `saas`, `minimal modern`, `electric blue`, `agency` | v1.0.4 |
| 6 | `design-template-luxury` | **Luxury Editorial** — Vogue / Hermès, Expensive Paper | `#F9F8F6` alabaster `#1A1A1A` charcoal `#D4AF37` gold | `Playfair Display` + `Inter` `6xl→9xl` `leading-[0.9]` | `0px`, `grayscale→color 1500ms`, vertical `writing-mode`, gold slide `translate-x`, ambient orbs | `luxury`, `editorial`, `vogue`, `chanel`, `expensive`, `tactile` | v1.0.5 |
| 7 | `design-template-terminal` | **Terminal CLI** — Hacker, Cyber-Industrial, Mainframe | `#0a0a0a` `#33ff00` green `#ffb000` amber `#1f521f` | `JetBrains Mono` `Fira Code` ALL CAPS headers | `0px`, `text-shadow 0 0 5px rgba(51,255,0,0.5)`, CRT scanlines, `[ BRACKETS ]` buttons, `user@host:~$` | `terminal`, `cli`, `hacker`, `shell`, `monospace`, `mainframe` | v1.0.6 |
| 8 | `design-template-swiss-minimalist` | **Swiss International** — Grid as Law, Helvetica Objectivity | `#FFFFFF` `#000000` `#F2F2F2` `#FF3000` Swiss Red | `Inter` 900/700 UPPERCASE `6xl→[10rem]` `tracking-tighter` | `0px` `border-4` visible grid, 4 patterns (grid 24px/dots 16px/diagonal/noise), Bauhaus compositions | `swiss`, `grid`, `international`, `helvetica`, `objective` | v1.0.7 |
| 9 | `design-template-kinetic` | **Kinetic Typography** — Poster Come to Life, Festival | `#09090B` `#FAFAFA` `#DFE104` acid yellow | `Space Grotesk` ALL UPPERCASE `clamp(3rem,12vw,14rem)` | `0px`, marquees speed 80/40 `react-fast-marquee`, hard inversions `#DFE104`, massive `8-12rem` numbers | `kinetic`, `marquee`, `acid yellow`, `brutalist type`, `poster` | v1.0.8 |
| 10 | `design-template-flat` | **Flat Design** — Confident Reduction, Poster Color Blocks | `#FFFFFF` `#111827` `#3B82F6` `#10B981` `#F59E0B` | `Outfit` 700/800 `-0.02em` | `shadow-none` absolute, `rounded-md/lg 6-8px`, `h-14/16` `hover:scale-105` | `flat`, `color block`, `poster`, `zero shadow` | v1.0.9 |
| 11 | `design-template-art-deco` | **Art Deco Gatsby** — Roaring Twenties, Metropolis | `#0A0A0A` obsidian `#F2F0E4` champagne `#D4AF37` gold | `Marcellus` + `Josefin Sans` 6xl/7xl uppercase | Stepped corners, rotated diamonds `45deg`, sunburst `radial-gradient`, double-frame, glow `0 0 15px rgba(212,175,55,0.2)` | `art deco`, `gatsby`, `roaring twenties`, `sunburst`, `zigzag` | v1.0.10 |
| 12 | `design-template-material` | **Material You M3** — Purple Seed Tonal, Google | `#FFFBFE` `#6750A4` `#E8DEF8` `#7D5260` | `Roboto` 400/500/700 | `rounded-full` pills, `24px` cards, `48px` hero, `blur-3xl` organic shapes, state layers `bg/90` | `material you`, `m3`, `google material`, `pill`, `tonal` | v1.0.11 |
| 13 | `design-template-neo-brutalism` | **Neo-brutalism** — Sticker Punk, Y2K Rave | `#FFFDF5` cream `#000000` `#FF6B6B` `#FFD93D` `#C4B5FD` | `Space Grotesk` 900 UPPERCASE `8xl→9xl` + `text-stroke 2px` | `border-4` black mandatory, `shadow-[8px_8px_0px_#000]` zero blur, rotated stickers `1/-2deg`, halftone | `neo brutalism`, `sticker`, `punk`, `y2k`, `hard shadow` | v1.0.12 |
| 14 | `design-template-bold-typography` | **Bold Typography** — Poster 6:1 Scale, Gallery | `#0A0A0A` `#FAFAFA` `#FF3D00` vermillion | `Inter Tight` + `Playfair Display` `5xl→8xl` `tracking-tighter -0.06em` | `0px`, underline `h-0.5` `scale-x-110` animated, layered muted text behind | `bold typography`, `poster`, `type hero`, `underline` | v1.0.13 |
| 15 | `design-template-academia` | **Academia Classical** — Mahogany Library, Brass | `#1C1714` mahogany `#E8DFD4` parchment `#C9A962` brass `#8B2635` crimson | `Cormorant Garamond` + `Crimson Pro` + `Cinzel` drop caps `7xl` | Arch-top `40% 40% 0 0 / 20%`, sepia `0.6→0` 700ms, corner flourishes 40px, wax seal `bg-[#8B2635]` | `academia`, `classical`, `library`, `brass`, `parchment`, `arch` | v1.0.14 |
| 16 | `design-template-cyberpunk` | **Cyberpunk Glitch** — High-Tech Low-Life, Blade Runner | `#0a0a0f` void `#00ff88` `#ff00ff` `#00d4ff` `#2a2a3a` | `Orbitron` + `Share Tech Mono` + `JetBrains Mono` `6xl→8xl` uppercase | Chamfer `clip-path 10px`, neon `0 0 5px #00ff88`, scanlines `repeating-linear 2/4px`, grid 50px 0.03, chromatic aberration | `cyberpunk`, `glitch`, `neon`, `matrix`, `blade runner`, `HUD` | v1.0.15 |
| 17 | `design-template-web3` | **Web3 Bitcoin DeFi** — Digital Gold, Luminescent | `#030304` void `#F7931A→#EA580C` orange `#FFD600` gold | `Space Grotesk` + `Inter` + `JetBrains Mono` | Glass `backdrop-blur-lg` + `border-white/10`, orbital rings `spin 10s`, grid 50px vignette, orange glow `0 0 20px` | `web3`, `bitcoin`, `defi`, `crypto`, `glass morphism` | v1.0.18 |
| 18 | `design-template-playful-geometric` | **Playful Geometric** — Memphis Sticker, Confetti | `#FFFDF5` cream `#8B5CF6` violet `#F472B6` `#FBBF24` `#34D399` | `Outfit` 700/800 + `Plus Jakarta Sans` | Blob `rounded-[100px] 20px` + `blur-3xl off-canvas`, hard shadow `4px 4px #1E293B` | `playful`, `memphis`, `sticker`, `confetti`, `pop` | v1.0.18 |
| 19 | `design-template-minimal-dark` | **Minimalist Dark** — Slate Atmospheric, Ember Glow | `#0A0A0F` `#12121A` `#1A1A24` `#F59E0B` amber | `Space Grotesk` + `Inter` + `JetBrains Mono` | Glass `rgba(26,26,36,0.6) blur 8px`, glow `0 0 20px rgba(245,158,11,0.4)`, border `white/0.08` | `minimal dark`, `slate + amber`, `atmospheric` | v1.0.18 |
| 20 | `design-template-claymorphism` | **Claymorphism** — Candy Clay Vinyl Toy | `#F4F1FA` `#7C3AED` `#DB2777` `#0EA5E9` `#332F3A` | `Nunito` 900 + `DM Sans` | `rounded-[60px]` hero `32px` card `20px` button, 4-layer clay shadows, squish `0.92` + breathe, blobs `60vh blur-3xl` | `claymorphism`, `clay`, `marshmallow`, `bouncy`, `inflated` | v1.0.23 |
| 21 | `design-template-profesional` | **Profesional Serif** — Ivory Book, Literary | `#FAFAF8` ivory `#1A1A1A` `#B8860B` gold | `Playfair Display` + `Source Sans 3` + `IBM Plex Mono` `7xl` | Rule lines `h-px` + small caps `0.15em`, `rounded-md` 6px, whitespace `py-32→44` | `profesional`, `serif`, `ivory`, `literary`, `book` | v1.0.23 |
| 22 | `design-template-botanical` | **Botanical Organic** — Garden Sage, Artisan | `#F9F8F4` alabaster `#2D3A31` forest `#8C9A84` sage `#C27B66` terracotta | `Playfair Display` italic 600/700 + `Source Sans 3` | Arch `rounded-t-full 200px`, paper grain `0.015` SVG noise, staggered `translate-y-12` | `botanical`, `organic`, `sage`, `garden`, `wellness` | v1.0.23 |
| 23 | `design-template-vaporwave` | **Vaporwave Outrun** — Neon Sunset 80s | `#090014` void `#FF00FF` `#00FFFF` `#FF9900` | `Orbitron` 900 + `Share Tech Mono` | Sunset gradient `FF9900→FF00FF→00FFFF`, `skew-x-12` buttons, perspective grid `rotateX 60deg`, CRT scanlines 4px, sun `600px blur 100px` | `vaporwave`, `outrun`, `synthwave`, `sunset gradient`, `80s` | v1.0.23 |
| 24 | `design-template-enterprise` | **Corporate Trust** — Indigo Unicorn, Poly | `#F8FAFC` slate `#4F46E5→#7C3AED` `#0F172A` | `Plus Jakarta Sans` 800 `4xl→6xl` | Soft colored shadows `rgba(79,70,229,0.1)`, `perspective-[2000px] rotate-x/y`, blur orbs `400-600px`, isometric | `enterprise`, `corporate`, `unicorn`, `indigo violet` | v1.0.23 |
| 25 | `design-template-sketch` | **Sketch Hand-Drawn** — Paper Doodle, Sticky Note | `#fdfbf7` paper `#2d2d2d` pencil `#ff4d4d` red `#2d5da1` blue `#fff9c4` post-it | `Kalam` 700 + `Patrick Hand` 400 | Wobbly `255px 15px 225px / ...`, hard offset `4px 4px #2d2d2d`, tape/tack, rotate `1-2deg`, dot grid 24px | `sketch`, `hand drawn`, `doodle`, `sticky note`, `wobbly` | v1.0.25 |
| 26 | `design-template-industrial` | **Industrial Skeuomorphism** — Braun Chassis, Teenage | `#e0e5ec` chassis `#2d3436` `#ff4757` orange `#babecc` | `Inter` 800 + `JetBrains Mono` mono labels | Dual neumorphic `8px 8px #babecc / -8px -8px #fff`, screws radial 12px, vents pill `inset`, pressed inputs | `industrial`, `skeuomorphism`, `neumorphism`, `mechanical` | v1.0.25 |
| 27 | `design-template-neumorphism` | **Neumorphism Soft UI** — Cool Clay Pillowed | `#E0E5EC` `#3D4852` `#6C63FF` `#38B2AC` | `Plus Jakarta Sans` 800 + `DM Sans` | RGBA dual `9px/12px rgb(163,177,198,0.6)`, `rounded-[32px]` `16px`, extruded `9px 9px` / pressed `inset 10px` | `neumorphism`, `soft ui`, `extruded`, `pillowed` | v1.0.29 |
| 28 | `design-template-organic` | **Organic Natural** — Wabi-sabi Blob | `#FDFCF8` rice `#2C2C24` `#5D7052` moss `#C18C5D` terracotta `#DED8CF` | `Fraunces` 600-800 + `Nunito 400` rounded | Blob `60% 40% 30% 70% / 60% 30% 70% 40%`, grain multiply `3-4%`, moss tinted shadows | `organic`, `natural`, `wabi-sabi`, `blob`, `earthy` | v1.0.29 |
| 29 | `design-template-maximalism` | **Maximalism Dopamine** — Lisa Frank Hyperpop | `#0D0D1A` `#FF3AF2` `#00F5D4` `#FFE600` `#FF6B35` `#7B2FFF` 5 accents | `Outfit 700-900` `7xl→9xl` + `DM Sans` | `border-4/8` clashing, triple `text-shadow 2px/4px/6px` rotating accents, dots 20px + stripes 45deg + checker + mesh radial, hard stacked `8→16→36px` | `maximalism`, `dopamine`, `hyperpop`, `lisa frank`, `more is more` | v1.0.29 |
| 30 | `design-template-retro` | **Retro 90s Nostalgia** — Windows 95 Geocities | `#C0C0C0` `#000000` `#0000FF` `#000080` navy `#FF0000` `#FFFF00` | `MS Sans Serif` + `Arial Black` UPPERCASE + `Courier New` mono | `0px` + bevel outset `border-color #fff #808080` + `inset -1px #404040`, rainbow `4s linear`, marquee, tiled `4px`, construction stripes `10px` | `retro`, `90s`, `geocities`, `windows 95`, `hit counter` | v1.0.29 |

> **Total: 30 templates + 2 utilities = 32 skills**

---

## Installation — Super Complete

Pick *one* — all point to the same source.

### 1 — npm / pnpm / yarn / bun (recommended)

> **Published as `muris11-design-template`** on npm (bare `design-template` was taken by an unrelated package).

```bash
# npm
npm install muris11-design-template

# pnpm
pnpm add muris11-design-template

# yarn
yarn add muris11-design-template

# bun
bun add muris11-design-template
```

Or install directly from GitHub:

```bash
npm install github:muris11/design-template
# or
npm install https://github.com/muris11/design-template/archive/refs/heads/main.tar.gz
```

**What you get:** Local `node_modules/muris11-design-template/skills/*` + `.claude-plugin/` auto-discovered by Claude Code.

Verify:
```bash
npm pack --dry-run  # should list 30+ SKILL.md + plugin.json
ls node_modules/muris11-design-template/skills | wc -l  # → 32
# skills.sh direct URL (live)
# https://www.skills.sh/muris11/design-template
```

### 2 — npx (one-shot, no install)

```bash
npx muris11-design-template@latest
# or via the installer
npx design-template@latest
```

The installer (`cli/index.mjs`) offers:
- Interactive picker (all / monochrome / bauhaus / …)
- Writes pointer block to `CLAUDE.md` / `AGENTS.md` / `GEMINI.md`
- Copies chosen `skills/*` next to your project

### 3 — skills.sh — The Agent Skills Directory

`design-template` is indexed on **[skills.sh](https://www.skills.sh)** — the global directory for agent skills (9700+ skills).

**Option A — skills CLI (recommended):**
```bash
# install the skills CLI once
npm install -g skills

# search
skills search design-template
# → shows all 30 templates with stars, weekly installs, description

# install one template globally
skills add muris11/design-template --skill design-template-monochrome

# install all templates
skills add muris11/design-template
```

**Option B — npx skills:**
```bash
npx skills add muris11/design-template --skill design-template-bauhaus
npx skills add muris11/design-template --skill design-template-cyberpunk
```

**Option C — Claude Code `plugin add`:**
```bash
# Claude Code discovers skills.sh sources automatically
/plugin add muris11/design-template
```

Verify on [skills.sh](https://www.skills.sh/muris11/design-template) — search `design-template` → you should see all 30 with install counts.

### 4 — Claude Code Plugin (native)

Claude Code v1.0+ auto-discovers plugins via `.claude-plugin/plugin.json`:

```bash
# inside your project
/plugin add muris11/design-template        # adds to .claude-plugin/marketplace.json
/plugin install design-template@latest
```

Or **local path** (dev):
```bash
/plugin add /absolute/path/to/design-template
```

Check:
```bash
/plugin list
# → design-template 1.0.29 — 32 skills: design-template, design-template-monochrome, ...
```

### 5 — OpenCode / OpenClaw / Cursor / Windsurf

All support the same `SKILL.md` frontmatter (`name`, `description`, `allowed-tools`):

```bash
# OpenCode
opencode skill add muris11/design-template

# Cursor — paste into .cursor/skills/
cp -r node_modules/muris11-design-template/skills/design-template-monochrome .cursor/skills/

# Windsurf — same
cp -r skills/design-template-modern-dark .windsurf/skills/
```

### 6 — Git Clone (for contributors)

```bash
git clone https://github.com/muris11/design-template.git
cd design-template
npm install
npm run sync-skills   # verifies name == folder for all 32 skills
npm test              # smoke-test loads each SKILL.md via skill tool
```

Add to your project via symlink during dev:
```bash
ln -s /path/to/design-template/skills/design-template-cyberpunk ./skills/design-template-cyberpunk
```

### 7 — Manual Copy-Paste (fastest for one template)

```bash
# copy a single template into your project
Copy-Item -Recurse node_modules/muris11-design-template/skills/design-template-luxury ./skills/design-template-luxury
```

No build step needed — the skill is just Markdown.

---

## Usage — From Idea to Shipped UI

### The 10-Second Flow

```text
You: "Redesign my pricing section with monochrome"
Agent: loads design-template-monochrome → reads #FFFFFF/#000000, Playfair Display, 0px, inversion
Agent: audits your stack (Next.js + Tailwind + shadcn), asks: "3 tiers or 4? Real prices?"
Agent: proposes plan (tokens → pricing card → page composition)
Agent: writes code in YOUR folder structure, explains why (R-01, inversion for emphasis)
Agent: runs Monochrome Checklist (0px? serif oversized? inversion? textures?)
→ Done.
```

### Loading a Skill

**Via skill tool (Claude Code / OpenCode):**
```
Skill: design-template-monochrome
Skill: design-template-bauhaus
Skill: design-template-cyberpunk
```

**Via prompt (any agent):**
> "Use the `design-template-neo-brutalism` skill. Redesign my hero in that style."

**Via loader (all at once):**
```
Skill: design-template-all   # loads all 32 → agent asks which vibe to apply
Skill: design-template       # loads core router → lists table → you pick
```

### Trigger Words Cheat Sheet

The `description` frontmatter is tuned so the agent auto-loads on natural language:

| Say this ... | Agent loads ... |
|---|---|
| `monochrome`, `black white`, `editorial`, `Vogue`, `no accent` | `monochrome` |
| `bauhaus`, `primary colors`, `geometric`, `constructivist` | `bauhaus` |
| `linear`, `vercel`, `raycast`, `dark premium`, `ambient glow` | `modern-dark` |
| `newspaper`, `broadsheet`, `journal`, `press` | `newsprint` |
| `saas`, `electric blue`, `agency`, `premium saas` | `saas` |
| `luxury`, `chanel`, `expensive`, `tactile paper` | `luxury` |
| `terminal`, `cli`, `hacker`, `mainframe`, `shell` | `terminal` |
| `swiss`, `grid`, `helvetica`, `objective` | `swiss-minimalist` |
| `kinetic`, `marquee`, `acid yellow`, `poster` | `kinetic` |
| `flat`, `color block`, `zero shadow` | `flat` |
| `art deco`, `gatsby`, `sunburst`, `zigzag` | `art-deco` |
| `material you`, `m3`, `pill`, `tonal` | `material` |
| `neo brutalism`, `sticker`, `y2k`, `hard shadow` | `neo-brutalism` |
| `bold typography`, `type hero`, `vermillon` | `bold-typography` |
| `academia`, `library`, `brass`, `parchment` | `academia` |
| `cyberpunk`, `glitch`, `neon`, `matrix`, `blade runner` | `cyberpunk` |
| `web3`, `bitcoin`, `defi`, `glass morphism` | `web3` |
| `playful`, `memphis`, `confetti`, `pop` | `playful-geometric` |
| `minimal dark`, `slate amber`, `atmospheric` | `minimal-dark` |
| `claymorphism`, `clay`, `marshmallow`, `bouncy` | `claymorphism` |
| `profesional`, `serif`, `literary`, `book` | `profesional` |
| `botanical`, `sage`, `terracotta`, `arch` | `botanical` |
| `vaporwave`, `outrun`, `sunset gradient`, `synthwave` | `vaporwave` |
| `enterprise`, `corporate trust`, `indigo violet` | `enterprise` |
| `sketch`, `hand drawn`, `wobbly`, `sticky note` | `sketch` |
| `industrial`, `skeuomorphism`, `neumorphism industrial` | `industrial` |
| `neumorphism`, `soft ui`, `pillowed` | `neumorphism` |
| `organic`, `wabi-sabi`, `blob`, `earthy` | `organic` |
| `maximalism`, `dopamine`, `hyperpop`, `lisa frank` | `maximalism` |
| `retro`, `90s`, `geocities`, `windows 95` | `retro` |

### Code Example — Next.js + Tailwind + shadcn

**Prompt:**
> "Use `design-template-bauhaus` to redesign my landing hero. Stack is Next.js 14 App Router + Tailwind + shadcn/ui."

**What the agent does (role section enforces this):**

1. **Audit** — reads `app/` structure, finds `components/ui/button.tsx`, `tailwind.config.ts`, `globals.css`, checks `Outfit` not loaded, sees `border-radius: 0.625rem` (conflicts with Bauhaus `rounded-none`)
2. **Ask** — "Redesign just the hero, or refactor buttons globally? Do you want red/blue/yellow as primary, or keep your brand hue?"
3. **Plan:**
   ```
   - Centralize tokens: update tailwind.config → borderRadius 0, colors { primary-red #D02020, blue #1040C0 }
   - Reusability: extend Button variants (primary-red / secondary-blue / yellow) before touching hero
   - Hero: asymmetric 60/40, left text (Outfit 900 uppercase), right geometric composition (overlapping circle+square+triangle)
   ```
4. **Code** — matches your patterns (`cn()` helper, `cva` variants), explains: "Bauhaus uses `rounded-none` + `border-4 #121212` + `shadow-[8px]` hard offset for constructivist depth — not soft shadows — because depth comes from color blocking, not blur"

### Checklist Before Ship

Every template ends with a checklist. The agent **must** run it:

```markdown
## Bauhaus Checklist
- [ ] Colors #F0F0F0 + #D02020/#1040C0/#F0C020 only + #121212 border?
- [ ] Outfit 900 uppercase tracking-tighter leading-[0.9]?
- [ ] border-4 #121212, shadow-[8px] hard, rounded-none/full binary?
- ...
```

No checklist = not shipped.

---

## Creating a New Template (30 seconds)

```powershell
# 1. Copy any template as starter
Copy-Item -Recurse skills/design-template-monochrome skills/design-template-mybrand

# 2. Edit frontmatter — name MUST equal folder
# skills/design-template-mybrand/SKILL.md
---
name: design-template-mybrand
description: "MyBrand — warm terracotta + cream, Canela serif, arch ... Use when user wants mybrand, terracotta, warm editorial."
---

# 3. Replace <role> if needed (usually keep) + replace <design-system> (tokens, components, motion)

# 4. Register in core router + loader (optional but recommended)
# → add row to skills/design-template/SKILL.md table
# → add line to skills/design-template-all/SKILL.md Steps: 1.

# 5. Bump version + push
# package.json + .claude-plugin/plugin.json → 1.0.30
git add . && git commit -m "feat: mybrand v1.0.30" && git tag v1.0.30 && git push origin main --tags
```

**Rules:**
- `name` == folder name (else skill won't load)
- One vibe = one skill. Don't mix tokens (Monochrome #000/#FFF vs Bauhaus primaries)
- Keep `<role>` (audit → ask → plan → code → explain) — it guarantees stack-idiomatic output

---

## Architecture & Files

```
design-template/
├── images/
│   └── cover.png                 # ← this README's cover
├── design-template.md            # core router document (human-readable index)
├── plugin.json                   # root plugin pointer
├── package.json                  # npm manifest (publish: muris11-design-template)
├── .claude-plugin/
│   └── plugin.json              # Claude Code manifest (skills: ["./skills/"], 32 skills)
├── rules/
│   └── design-template.md       # copy of core for linters
├── skills/
│   ├── design-template/SKILL.md              # CORE — router + picker
│   ├── design-template-all/SKILL.md          # LOADER — loads all 30
│   ├── design-template-monochrome/SKILL.md   # template skills (30×)
│   └── ...
└── cli/                          # (optional) installer + sync-skills
```

**Frontmatter contract (required):**
```yaml
---
name: design-template-<kebab>   # MUST equal folder
description: "<vibe> — <1-line>. Use when user wants <trigger words>."
allowed-tools: Read Write Edit Glob Grep
---
```

**Internal structure (every template):**
```md
<role>            # HOW the agent works — stack audit → ask → plan → code → explain
<design-system>   # WHAT the agent builds — Philosophy, Tokens, Components, Layout, Motion, Bold Factor
## How to use this skill
## <Template> Checklist   # Verification before delivery
```

---

## FAQ

**Q: Do I need to install all 30 templates?**
No. Copy *one* `skills/design-template-*` you need. Or use `skills add muris11/design-template --skill design-template-cyberpunk` to pull just that one.

**Q: Will it overwrite my Tailwind config?**
No. The agent *proposes* a plan first (centralize tokens vs adapt). You approve. Tokens are suggested as CSS variables + `tailwind.config` diff, not forced overwrite.

**Q: Does it work outside Claude Code?**
Yes. Any agent that reads `SKILL.md` (OpenCode, Cursor, Windsurf, Copilot) can use the `<role>` + `<design-system>`. The `allowed-tools` frontmatter is advisory — ignore if your harness doesn't support it.

**Q: npm name?**
Published as **`muris11-design-template`** on npm (bare `design-template` was taken by an unrelated package `v2.0.35`):
```bash
npm install muris11-design-template
# then alias if you want
ln -s node_modules/muris11-design-template ./design-template
```

**Q: How does skills.sh indexing work?**
On `npm publish`, npm's webhook notifies skills.sh. Within 5-15 min, your versions appear at `https://www.skills.sh/muris11/design-template`. No manual `skills publish` needed. You can also `npx skills add muris11/design-template` to force a re-index.

**Q: Can I mix two templates (e.g., Bauhaus grid + Cyberpunk neon)?**
Don't. Each template's palette/radius/shadow system is intentionally closed ("Monochrome is absolute"). Mixing breaks the vibe. Pick one vibe per page/section. If you truly need hybrid, create a *new* template (copy one, remix tokens, give it a new name).

**Q: License?**
MIT — commercial use, attribution appreciated but not required. See [`LICENSE`](./LICENSE).

---

## Versioning & Changelog

We use **SemVer**: `1.0.x` patch = new template, `1.x.0` minor = breaking token change, `x.0.0` major = skill contract change.

| Version | Date | What |
|---------|------|------|
| `1.0.29` | 2025-09-03 | + neumorphism, organic, maximalism, retro (4) |
| `1.0.25` | 2025-09-03 | + sketch, industrial (2) |
| `1.0.23` | 2025-09-03 | + claymorphism, profesional, botanical, vaporwave, enterprise (5) |
| `1.0.18` | 2025-09-03 | + web3, playful-geometric, minimal-dark (3, batch) |
| `1.0.15` | 2025-09-03 | + cyberpunk |
| `1.0.14` | 2025-09-03 | + academia |
| `1.0.13` | 2025-09-03 | + bold-typography |
| `1.0.12` | 2025-09-03 | + neo-brutalism |
| `1.0.11` | 2025-09-03 | + material |
| `1.0.10` | 2025-09-03 | + art-deco |
| `1.0.09` | 2025-09-03 | + flat |
| `1.0.08` | 2025-09-03 | + kinetic |
| `1.0.07` | 2025-09-03 | + swiss-minimalist |
| `1.0.06` | 2025-09-03 | + terminal |
| `1.0.05` | 2025-09-03 | + luxury |
| `1.0.04` | 2025-09-03 | + saas |
| `1.0.03` | 2025-09-03 | + newsprint |
| `1.0.02` | 2025-09-03 | + modern-dark |
| `1.0.01` | 2025-09-03 | + bauhaus |
| `1.0.00` | 2025-09-03 | + monochrome (core + all + router) |

Full log: `git log --oneline --graph --all` and GitHub Releases (tags `v1.0.x`).

---

## Contributing

```bash
git clone https://github.com/muris11/design-template.git
cd design-template
# create a template
Copy-Item -Recurse skills/design-template-monochrome skills/design-template-mybrand
# edit SKILL.md → name + description + <design-system>
npm run sync-skills   # verifies name == folder
npm test              # smoke-test loads each skill
git add . && git commit -m "feat: mybrand v1.0.30" && git push
```

PRs welcome — please keep one template per PR, include the Checklist, and keep the role intact.

---

## Credits & License

Built by [@muris11](https://github.com/muris11) — wrapping **30 design identities** from Swiss grid law to vaporwave neon into skills your agent can *actually* use.

Design inspiration: Bauhaus, Swiss International, Vogue, Linear, Vercel, Braun / Teenage Engineering, Material You, and the open web.

**License:** [MIT](./LICENSE) — do anything, just keep the notice.

<p align="center">
  <sub>If <code>design-template</code> saved you a week of token bikeshedding, give it a ⭐ on <a href="https://github.com/muris11/design-template">GitHub</a> and a <code>skills add</code> on <a href="https://www.skills.sh/muris11/design-template">skills.sh</a> — it takes 5 seconds and keeps the lights on.</sub>
</p>

<p align="center">
  <img src="images/cover.png" alt="design-template — 30 identities" width="100%" />
</p>
