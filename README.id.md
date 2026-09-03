<p align="center">
  <img src="images/cover.png" alt="cover design-template" width="100%" />
</p>

<h1 align="center">design-template</h1>

<p align="center">
  <strong>30+ Design System Siap Pakai sebagai Agent Skills</strong><br/>
  Token murni. Tanpa tebak-tebakan. Tiap skill = satu <code>&lt;role&gt;</code> + <code>&lt;design-system&gt;</code> lengkap siap drop ke codebase apapun.
</p>

<p align="center">
  <a href="https://github.com/muris11/design-template"><img src="https://img.shields.io/github/stars/muris11/design-template?style=flat&label=Stars" alt="GitHub Stars" /></a>
  <a href="https://www.npmjs.com/package/muris11-design-template"><img src="https://img.shields.io/npm/v/muris11-design-template?label=npm&color=CB0000" alt="npm version" /></a>
  <a href="https://www.skills.sh/muris11/design-template"><img src="https://img.shields.io/badge/skills.sh-design--template-7C3AED" alt="skills.sh" /></a>
  <a href="https://github.com/muris11/design-template/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-green" alt="MIT" /></a>
  <img src="https://img.shields.io/badge/skills-30%2B-0A0A0A" alt="30+ Skills" />
  <img src="https://img.shields.io/badge/Claude%20Code-Compatible-5E6AD2" alt="Claude Code" />
</p>

<p align="center">
  <a href="./README.md">🇬🇧 English</a> · <a href="#instalasi">Instalasi</a> · <a href="#katalog-skill">Katalog</a> · <a href="#cara-pakai">Cara Pakai</a> · <a href="https://github.com/muris11/design-template/issues">Issues</a>
</p>

---

## Apa itu `design-template`?

`design-template` **bukan component library**. Ini adalah **koleksi 30 identitas desain** yang dikemas sebagai **agent skills** (`SKILL.md`) untuk AI coding agent (Claude Code, OpenCode, Cursor, Windsurf, Copilot).

Tiap sub-skill itu **self-contained**: satu `<role>` (gimana agent kerja) + satu `<design-system>` (token, komponen, layout, motion, texture) + **checklist verifikasi**.

```
design-template/
├── design-template.md            # core router — daftar semua template
├── skills/
│   ├── design-template/          # CORE — router skill (daftar, picker)
│   ├── design-template-all/      # LOADER — load semua sekaligus
│   ├── design-template-monochrome/    # Pure B&W editorial
│   ├── design-template-bauhaus/       # Primaries + hard shadows
│   ├── design-template-swiss-minimalist/ # Swiss grid law
│   ├── ... 27 template lagi ...
│   └── design-template-retro/         # Windows 95 90s nostalgia
```

**Kenapa skills, bukan npm components?**

| Cara lama (components) | Cara baru (skills) |
|---|---|
| Install library, berantem sama API-nya | Agent *baca* DNA desainnya, nulis kode di *stack lu* |
| Kekunci React/Vue | Jalan di stack apapun: React, Next.js, Vue, Svelte, HTML, Tailwind, shadcn |
| Output generik | Output beropini & deliberate — tiap token ada alasannya |

> **Satu perintah:** Agent load `design-template-monochrome` → langsung tau `#000/#FFF only`, `Playfair Display`, `0px`, `inversion`, tanpa shadow — dan nulis kode yang pas.

---

## Fitur

- **30 template** — dari Minimalist Monochrome sampai Vaporwave sampai Brutalist — tiap template 400-800 baris spec yang actionable
- **Fidelity 100%** — tiap warna, radius, shadow, grid, type scale bisa dicopy-paste sebagai Tailwind / CSS
- **Role + System + Checklist** — tiap skill maksa agent audit stack lu → nanya scope → bikin plan → nulis kode → verifikasi via checklist
- **Stack-agnostic** — React, Next.js, Vue, Svelte, Astro, HTML — agent adaptasi ke *pattern lu*
- **Claude Code native** — auto-ke-detect via `.claude-plugin/plugin.json` (`skills: ["./skills/"]`)
- **skills.sh & npm ready** — install via `npx skills add`, `npm i`, atau git clone
- **Copy-paste buat bikin baru** — `Copy-Item design-template-monochrome design-template-mybrand` — beres

---

## Katalog Skill — 30 Template + 2 Utilitas

> **Cara pilih:** Cari vibe lu → catat nama skill → load. Agent yang ngurus sisanya.

| # | Skill | Vibe & Keyword | Palette | Typography | Signature | Trigger Words | Sejak |
|---|-------|----------------|---------|------------|-----------|---------------|-------|
| 0 | `design-template` | **CORE router** — daftar semua template | — | — | Tabel picker | `design-template`, `list templates` | v1.0.0 |
| 0 | `design-template-all` | **LOADER** — load semua 30 sekaligus | — | — | One-shot loader | `design-template semua`, `all` | v1.0.0 |
| 1 | `design-template-monochrome` | **Minimalist Monochrome** — Editorial Luxury Austere, Vogue / Celine | `#FFFFFF` `#000000` only | `Playfair Display` serif hero `8xl→9xl`, `JetBrains Mono` labels | 0px everywhere, inversion, horizontal-line texture 1.5%, hero oversized type | `monochrome`, `black white`, `editorial`, `luxury`, `Vogue`, `no accent` | v1.0.0 |
| 2 | `design-template-bauhaus` | **Bauhaus** — Konstruktivis, Modernis, Poster 1920s | `#F0F0F0` + `#D02020` `#1040C0` `#F0C020` + `#121212` | `Outfit` 400/500/700/900 | `border-4` `#121212`, `shadow-[8px]` hard, `rounded-none/full` binary | `bauhaus`, `constructivist`, `geometric`, `primary colors` | v1.0.1 |
| 3 | `design-template-modern-dark` | **Modern Dark (Linear)** — Deep Space Sinematik, Raycast / Linear | `#050506` `#020203` `#5E6AD2` `#EDEDEF` | `Inter` / `Geist Sans` `tracking-[-0.03em]` | 4-layer bg (radial + noise + blobs `150px` + grid 64px), spotlight 300px, parallax | `modern dark`, `linear`, `vercel`, `raycast`, `ambient glow` | v1.0.2 |
| 4 | `design-template-newsprint` | **Newsprint** — Jurnalisme Golden Age, NY Times | `#F9F9F7` paper `#111111` ink `#CC0000` red | `Playfair Display` + `Lora` + `Inter` + `JetBrains Mono` `9xl` `leading-[0.9]` | `0px` + collapsed `border-r/b` grids + `hard 4px` shadow + dot/line textures + drop caps + Vol.1 | `newsprint`, `newspaper`, `broadsheet`, `journal`, `press` | v1.0.3 |
| 5 | `design-template-saas` | **Minimalist Modern SaaS** — SaaS Agency Premium | `#FAFAFA` `#0F172A` `#0052FF→#4D7CFF` | `Calistoga` + `Inter` + `JetBrains Mono` | Gradient `#0052FF` signature, inverted slate sections, floating cards 5s, pulsing dot, `rounded-xl/2xl` | `saas`, `minimal modern`, `electric blue`, `agency` | v1.0.4 |
| 6 | `design-template-luxury` | **Luxury Editorial** — Vogue / Hermès, Kertas Mahal | `#F9F8F6` alabaster `#1A1A1A` charcoal `#D4AF37` gold | `Playfair Display` + `Inter` `6xl→9xl` `leading-[0.9]` | `0px`, `grayscale→color 1500ms`, vertical `writing-mode`, gold slide `translate-x`, ambient orbs | `luxury`, `editorial`, `vogue`, `chanel`, `expensive`, `tactile` | v1.0.5 |
| 7 | `design-template-terminal` | **Terminal CLI** — Hacker, Cyber-Industrial, Mainframe | `#0a0a0a` `#33ff00` green `#ffb000` amber `#1f521f` | `JetBrains Mono` `Fira Code` ALL CAPS headers | `0px`, `text-shadow 0 0 5px rgba(51,255,0,0.5)`, CRT scanlines, `[ BRACKETS ]` buttons, `user@host:~$` | `terminal`, `cli`, `hacker`, `shell`, `monospace`, `mainframe` | v1.0.6 |
| 8 | `design-template-swiss-minimalist` | **Swiss International** — Grid as Law, Helvetica Objektif | `#FFFFFF` `#000000` `#F2F2F2` `#FF3000` Swiss Red | `Inter` 900/700 UPPERCASE `6xl→[10rem]` `tracking-tighter` | `0px` `border-4` visible grid, 4 patterns (grid 24px/dots 16px/diagonal/noise), Bauhaus compositions | `swiss`, `grid`, `international`, `helvetica`, `objective` | v1.0.7 |
| 9 | `design-template-kinetic` | **Kinetic Typography** — Poster Hidup, Festival | `#09090B` `#FAFAFA` `#DFE104` acid yellow | `Space Grotesk` ALL UPPERCASE `clamp(3rem,12vw,14rem)` | `0px`, marquees speed 80/40 `react-fast-marquee`, hard inversions `#DFE104`, massive `8-12rem` numbers | `kinetic`, `marquee`, `acid yellow`, `brutalist type`, `poster` | v1.0.8 |
| 10 | `design-template-flat` | **Flat Design** — Confident Reduction, Poster Color Blocks | `#FFFFFF` `#111827` `#3B82F6` `#10B981` `#F59E0B` | `Outfit` 700/800 `-0.02em` | `shadow-none` absolute, `rounded-md/lg 6-8px`, `h-14/16` `hover:scale-105` | `flat`, `color block`, `poster`, `zero shadow` | v1.0.9 |
| 11 | `design-template-art-deco` | **Art Deco Gatsby** — Roaring Twenties, Metropolis | `#0A0A0A` obsidian `#F2F0E4` champagne `#D4AF37` gold | `Marcellus` + `Josefin Sans` 6xl/7xl uppercase | Stepped corners, rotated diamonds `45deg`, sunburst `radial-gradient`, double-frame, glow `0 0 15px rgba(212,175,55,0.2)` | `art deco`, `gatsby`, `roaring twenties`, `sunburst`, `zigzag` | v1.0.10 |
| 12 | `design-template-material` | **Material You M3** — Purple Seed Tonal, Google | `#FFFBFE` `#6750A4` `#E8DEF8` `#7D5260` | `Roboto` 400/500/700 | `rounded-full` pills, `24px` cards, `48px` hero, `blur-3xl` organic shapes, state layers `bg/90` | `material you`, `m3`, `google material`, `pill`, `tonal` | v1.0.11 |
| 13 | `design-template-neo-brutalism` | **Neo-brutalism** — Sticker Punk, Y2K Rave | `#FFFDF5` cream `#000000` `#FF6B6B` `#FFD93D` `#C4B5FD` | `Space Grotesk` 900 UPPERCASE `8xl→9xl` + `text-stroke 2px` | `border-4` black mandatory, `shadow-[8px_8px_0px_#000]` zero blur, rotated stickers `1/-2deg`, halftone | `neo brutalism`, `sticker`, `punk`, `y2k`, `hard shadow` | v1.0.12 |
| 14 | `design-template-bold-typography` | **Bold Typography** — Poster 6:1 Scale, Gallery | `#0A0A0A` `#FAFAFA` `#FF3D00` vermillion | `Inter Tight` + `Playfair Display` `5xl→8xl` `tracking-tighter -0.06em` | `0px`, underline `h-0.5` `scale-x-110` animated, layered muted text | `bold typography`, `poster`, `type hero`, `underline` | v1.0.13 |
| 15 | `design-template-academia` | **Academia Classical** — Mahogany Library, Brass | `#1C1714` mahogany `#E8DFD4` parchment `#C9A962` brass `#8B2635` crimson | `Cormorant Garamond` + `Crimson Pro` + `Cinzel` drop caps `7xl` | Arch-top `40% 40% 0 0 / 20%`, sepia `0.6→0` 700ms, corner flourishes 40px, wax seal `bg-[#8B2635]` | `academia`, `classical`, `library`, `brass`, `parchment`, `arch` | v1.0.14 |
| 16 | `design-template-cyberpunk` | **Cyberpunk Glitch** — High-Tech Low-Life, Blade Runner | `#0a0a0f` void `#00ff88` `#ff00ff` `#00d4ff` `#2a2a3a` | `Orbitron` + `Share Tech Mono` + `JetBrains Mono` `6xl→8xl` uppercase | Chamfer `clip-path 10px`, neon `0 0 5px #00ff88`, scanlines `repeating-linear 2/4px`, grid 50px 0.03, chromatic aberration | `cyberpunk`, `glitch`, `neon`, `matrix`, `blade runner`, `HUD` | v1.0.15 |
| 17 | `design-template-web3` | **Web3 Bitcoin DeFi** — Digital Gold, Luminescent | `#030304` void `#F7931A→#EA580C` orange `#FFD600` gold | `Space Grotesk` + `Inter` + `JetBrains Mono` | Glass `backdrop-blur-lg` + `border-white/10`, orbital rings `spin 10s`, grid 50px vignette, orange glow `0 0 20px` | `web3`, `bitcoin`, `defi`, `crypto`, `glass morphism` | v1.0.18 |
| 18 | `design-template-playful-geometric` | **Playful Geometric** — Memphis Sticker, Confetti | `#FFFDF5` cream `#8B5CF6` violet `#F472B6` `#FBBF24` `#34D399` | `Outfit` 700/800 + `Plus Jakarta Sans` | Blob `rounded-[100px] 20px` + `blur-3xl off-canvas`, hard shadow `4px 4px #1E293B` | `playful`, `memphis`, `sticker`, `confetti`, `pop` | v1.0.18 |
| 19 | `design-template-minimal-dark` | **Minimalist Dark** — Slate Atmospheric, Ember Glow | `#0A0A0F` `#12121A` `#1A1A24` `#F59E0B` amber | `Space Grotesk` + `Inter` + `JetBrains Mono` | Glass `rgba(26,26,36,0.6) blur 8px`, glow `0 0 20px rgba(245,158,11,0.4)`, border `white/0.08` | `minimal dark`, `slate amber`, `atmospheric` | v1.0.18 |
| 20 | `design-template-claymorphism` | **Claymorphism** — Candy Clay Vinyl Toy | `#F4F1FA` `#7C3AED` `#DB2777` `#0EA5E9` `#332F3A` | `Nunito` 900 + `DM Sans` | `rounded-[60px]` hero `32px` card `20px` button, 4-layer clay shadows, squish `0.92` + breathe, blobs `60vh blur-3xl` | `claymorphism`, `clay`, `marshmallow`, `bouncy`, `inflated` | v1.0.23 |
| 21 | `design-template-profesional` | **Profesional Serif** — Ivory Book, Literary | `#FAFAF8` ivory `#1A1A1A` `#B8860B` gold | `Playfair Display` + `Source Sans 3` + `IBM Plex Mono` `7xl` | Rule lines `h-px` + small caps `0.15em`, `rounded-md` 6px, whitespace `py-32→44` | `profesional`, `serif`, `ivory`, `literary`, `book` | v1.0.23 |
| 22 | `design-template-botanical` | **Botanical Organic** — Garden Sage, Artisan | `#F9F8F4` alabaster `#2D3A31` forest `#8C9A84` sage `#C27B66` terracotta | `Playfair Display` italic 600/700 + `Source Sans 3` | Arch `rounded-t-full 200px`, paper grain `0.015` SVG noise, staggered `translate-y-12` | `botanical`, `organic`, `sage`, `garden`, `wellness` | v1.0.23 |
| 23 | `design-template-vaporwave` | **Vaporwave Outrun** — Neon Sunset 80s | `#090014` void `#FF00FF` `#00FFFF` `#FF9900` | `Orbitron` 900 + `Share Tech Mono` | Sunset gradient `FF9900→FF00FF→00FFFF`, `skew-x-12` buttons, perspective grid `rotateX 60deg`, CRT scanlines 4px, sun `600px blur 100px` | `vaporwave`, `outrun`, `synthwave`, `sunset gradient`, `80s` | v1.0.23 |
| 24 | `design-template-enterprise` | **Corporate Trust** — Indigo Unicorn, Polished | `#F8FAFC` slate `#4F46E5→#7C3AED` `#0F172A` | `Plus Jakarta Sans` 800 `4xl→6xl` | Soft colored shadows `rgba(79,70,229,0.1)`, `perspective-[2000px] rotate-x/y`, blur orbs `400-600px`, isometric | `enterprise`, `corporate`, `unicorn`, `indigo violet` | v1.0.23 |
| 25 | `design-template-sketch` | **Sketch Hand-Drawn** — Paper Doodle, Sticky Note | `#fdfbf7` paper `#2d2d2d` pencil `#ff4d4d` red `#2d5da1` blue `#fff9c4` post-it | `Kalam` 700 + `Patrick Hand` 400 | Wobbly `255px 15px 225px / ...`, hard offset `4px 4px #2d2d2d`, tape/tack, rotate `1-2deg`, dot grid 24px | `sketch`, `hand drawn`, `doodle`, `sticky note`, `wobbly` | v1.0.25 |
| 26 | `design-template-industrial` | **Industrial Skeuomorphism** — Braun Chassis, Teenage | `#e0e5ec` chassis `#2d3436` `#ff4757` orange `#babecc` | `Inter` 800 + `JetBrains Mono` mono labels | Dual neumorphic `8px 8px #babecc / -8px -8px #fff`, screws radial 12px, vents pill `inset`, pressed inputs | `industrial`, `skeuomorphism`, `neumorphism`, `mechanical` | v1.0.25 |
| 27 | `design-template-neumorphism` | **Neumorphism Soft UI** — Cool Clay Pillowed | `#E0E5EC` `#3D4852` `#6C63FF` `#38B2AC` | `Plus Jakarta Sans` 800 + `DM Sans` | RGBA dual `9px/12px rgb(163,177,198,0.6)`, `rounded-[32px]` `16px`, extruded `9px 9px` / pressed `inset 10px` | `neumorphism`, `soft ui`, `extruded`, `pillowed` | v1.0.29 |
| 28 | `design-template-organic` | **Organic Natural** — Wabi-sabi Blob | `#FDFCF8` rice `#2C2C24` `#5D7052` moss `#C18C5D` terracotta `#DED8CF` | `Fraunces` 600-800 + `Nunito 400` rounded | Blob `60% 40% 30% 70% / 60% 30% 70% 40%`, grain multiply `3-4%`, moss tinted shadows | `organic`, `natural`, `wabi-sabi`, `blob`, `earthy` | v1.0.29 |
| 29 | `design-template-maximalism` | **Maximalism Dopamine** — Lisa Frank Hyperpop | `#0D0D1A` `#FF3AF2` `#00F5D4` `#FFE600` `#FF6B35` `#7B2FFF` 5 accents | `Outfit 700-900` `7xl→9xl` + `DM Sans` | `border-4/8` clashing, triple `text-shadow 2px/4px/6px` rotating accents, dots 20px + stripes 45deg + checker + mesh radial, hard stacked `8→16→36px` | `maximalism`, `dopamine`, `hyperpop`, `lisa frank`, `more is more` | v1.0.29 |
| 30 | `design-template-retro` | **Retro 90s Nostalgia** — Windows 95 Geocities | `#C0C0C0` `#000000` `#0000FF` `#000080` navy `#FF0000` `#FFFF00` | `MS Sans Serif` + `Arial Black` UPPERCASE + `Courier New` mono | `0px` + bevel outset `border-color #fff #808080` + `inset -1px #404040`, rainbow `4s linear`, marquee, tiled `4px`, construction stripes `10px` | `retro`, `90s`, `geocities`, `windows 95`, `hit counter` | v1.0.29 |

> **Total: 30 template + 2 utilitas = 32 skills**

---

## Instalasi — Super Lengkap

Pilih *satu* — semuanya menuju sumber yang sama.

### 1 — npm / pnpm / yarn / bun (direkomendasikan)

> **Publish sebagai `muris11-design-template`** di npm (bare `design-template` sudah diambil package lain).

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

Atau install langsung dari GitHub:

```bash
npm install github:muris11/design-template
# atau
npm install https://github.com/muris11/design-template/archive/refs/heads/main.tar.gz
```

**Yang lu dapat:** Lokal `node_modules/muris11-design-template/skills/*` + `.claude-plugin/` auto-ke-detect Claude Code.

Verifikasi:
```bash
npm pack --dry-run  # harus list 30+ SKILL.md + plugin.json
ls node_modules/muris11-design-template/skills | wc -l  # → 32
# skills.sh direct URL (live)
# https://www.skills.sh/muris11/design-template
```

### 2 — npx (one-shot, tanpa install)

```bash
npx muris11-design-template@latest
# atau via installer
npx design-template@latest
```

Installer (`cli/index.mjs`) menawarkan:
- Picker interaktif (all / monochrome / bauhaus / …)
- Nulis pointer block ke `CLAUDE.md` / `AGENTS.md` / `GEMINI.md`
- Copy `skills/*` yang dipilih ke sebelah project lu

### 3 — skills.sh — The Agent Skills Directory

`design-template` terindex di **[skills.sh](https://www.skills.sh)** — direktori global untuk agent skills (9700+ skills).

**Opsi A — skills CLI (direkomendasikan):**
```bash
# install skills CLI sekali
npm install -g skills

# cari
skills search design-template
# → nampilin semua 30 template dengan stars, weekly installs, deskripsi

# install satu template global
skills add muris11/design-template --skill design-template-monochrome

# install semua template
skills add muris11/design-template
```

**Opsi B — npx skills:**
```bash
npx skills add muris11/design-template --skill design-template-bauhaus
npx skills add muris11/design-template --skill design-template-cyberpunk
```

**Opsi C — Claude Code `plugin add`:**
```bash
# Claude Code auto-discover source skills.sh
/plugin add muris11/design-template
```

Verifikasi di [skills.sh](https://www.skills.sh/muris11/design-template) — search `design-template` → harus muncul semua 30 dengan install counts.

### 4 — Claude Code Plugin (native)

Claude Code v1.0+ auto-discover plugins via `.claude-plugin/plugin.json`:

```bash
# di dalam project lu
/plugin add muris11/design-template        # adds to .claude-plugin/marketplace.json
/plugin install design-template@latest
```

Atau **local path** (dev):
```bash
/plugin add /absolute/path/to/design-template
```

Cek:
```bash
/plugin list
# → design-template 1.0.29 — 32 skills: design-template, design-template-monochrome, ...
```

### 5 — OpenCode / OpenClaw / Cursor / Windsurf

Semua support frontmatter `SKILL.md` yang sama (`name`, `description`, `allowed-tools`):

```bash
# OpenCode
opencode skill add muris11/design-template

# Cursor — paste ke .cursor/skills/
cp -r node_modules/muris11-design-template/skills/design-template-monochrome .cursor/skills/

# Windsurf — sama
cp -r skills/design-template-modern-dark .windsurf/skills/
```

### 6 — Git Clone (buat kontributor)

```bash
git clone https://github.com/muris11/design-template.git
cd design-template
npm install
npm run sync-skills   # verifikasi name == folder untuk semua 32 skills
npm test              # smoke-test load tiap SKILL.md via skill tool
```

Tambah ke project via symlink saat dev:
```bash
ln -s /path/to/design-template/skills/design-template-cyberpunk ./skills/design-template-cyberpunk
```

### 7 — Manual Copy-Paste (paling cepet buat satu template)

```bash
# copy satu template ke project lu
Copy-Item -Recurse node_modules/muris11-design-template/skills/design-template-luxury ./skills/design-template-luxury
```

Gak perlu build step — skill cuma Markdown.

---

## Cara Pakai — Dari Ide ke UI Jadi

### Flow 10-Detik

```text
Lu: "Redesign pricing section gua pakai monochrome"
Agent: load design-template-monochrome → baca #FFFFFF/#000000, Playfair Display, 0px, inversion
Agent: audit stack lu (Next.js + Tailwind + shadcn), nanya: "3 tier atau 4? Harga real berapa?"
Agent: propose plan (tokens → pricing card → page composition)
Agent: nulis kode di folder structure LU, jelasin kenapa (R-01, inversion buat emphasis)
Agent: jalanin Monochrome Checklist (0px? serif oversized? inversion? textures?)
→ Beres.
```

### Cara Load Skill

**Via skill tool (Claude Code / OpenCode):**
```
Skill: design-template-monochrome
Skill: design-template-bauhaus
Skill: design-template-cyberpunk
```

**Via prompt (agent apapun):**
> "Pakai skill `design-template-neo-brutalism`. Redesign hero gua pakai style itu."

**Via loader (semua sekaligus):**
```
Skill: design-template-all   # load semua 32 → agent nanya vibe mana yang dipakai
Skill: design-template       # load core router → nampilin tabel → lu pilih
```

### Cheat Sheet Trigger Words

Frontmatter `description` di-tuning biar agent auto-load dari bahasa natural:

| Lu bilang ... | Agent load ... |
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

### Contoh Kode — Next.js + Tailwind + shadcn

**Prompt:**
> "Pakai `design-template-bauhaus` buat redesign landing hero gua. Stack Next.js 14 App Router + Tailwind + shadcn/ui."

**Yang agent lakuin (role section maksa ini):**

1. **Audit** — baca struktur `app/`, nemu `components/ui/button.tsx`, `tailwind.config.ts`, `globals.css`, cek `Outfit` belum ke-load, lihat `border-radius: 0.625rem` (tabrakan sama Bauhaus `rounded-none`)
2. **Nanya** — "Redesign cuma hero, atau refactor buttons global? Mau red/blue/yellow sebagai primary, atau keep brand hue lu?"
3. **Plan:**
   ```
   - Centralize tokens: update tailwind.config → borderRadius 0, colors { primary-red #D02020, blue #1040C0 }
   - Reusability: extend Button variants (primary-red / secondary-blue / yellow) sebelum sentuh hero
   - Hero: asymmetric 60/40, kiri text (Outfit 900 uppercase), kanan geometric composition (overlapping circle+square+triangle)
   ```
4. **Code** — ngikutin pattern lu (`cn()` helper, `cva` variants), jelasin: "Bauhaus pakai `rounded-none` + `border-4 #121212` + `shadow-[8px]` hard offset buat depth konstruktivis — bukan soft shadow — karena depth datang dari color blocking, bukan blur"

### Checklist Sebelum Ship

Tiap template diakhiri checklist. Agent **wajib** jalanin:

```markdown
## Bauhaus Checklist
- [ ] Colors #F0F0F0 + #D02020/#1040C0/#F0C020 only + #121212 border?
- [ ] Outfit 900 uppercase tracking-tighter leading-[0.9]?
- [ ] border-4 #121212, shadow-[8px] hard, rounded-none/full binary?
- ...
```

Gak ada checklist = belum ship.

---

## Bikin Template Baru (30 detik)

```powershell
# 1. Copy template apapun sebagai starter
Copy-Item -Recurse skills/design-template-monochrome skills/design-template-mybrand

# 2. Edit frontmatter — name HARUS sama dengan folder
# skills/design-template-mybrand/SKILL.md
---
name: design-template-mybrand
description: "MyBrand — warm terracotta + cream, Canela serif, arch ... Use when user wants mybrand, terracotta, warm editorial."
---

# 3. Ganti <role> kalau perlu (biasanya keep) + ganti <design-system> (tokens, components, motion)

# 4. Daftarin di core router + loader (opsional tapi direkomendasi)
# → tambah baris di skills/design-template/SKILL.md tabel
# → tambah baris di skills/design-template-all/SKILL.md Steps: 1.

# 5. Bump version + push
# package.json + .claude-plugin/plugin.json → 1.0.30
git add . && git commit -m "feat: mybrand v1.0.30" && git tag v1.0.30 && git push origin main --tags
```

**Aturan:**
- `name` == nama folder (kalau beda skill gak ke-load)
- Satu vibe = satu skill. Jangan campur token (Monochrome #000/#FFF vs Bauhaus primaries)
- Keep `<role>` (audit → nanya → plan → code → jelasin) — itu yang jamin output stack-idiomatic

---

## Arsitektur & Files

```
design-template/
├── images/
│   └── cover.png                 # ← cover README ini
├── design-template.md            # core router document (human-readable index)
├── plugin.json                   # root plugin pointer
├── package.json                  # npm manifest (publish: muris11-design-template)
├── .claude-plugin/
│   └── plugin.json              # Claude Code manifest (skills: ["./skills/"], 32 skills)
├── rules/
│   └── design-template.md       # copy core buat linters
├── skills/
│   ├── design-template/SKILL.md              # CORE — router + picker
│   ├── design-template-all/SKILL.md          # LOADER — load semua 30
│   ├── design-template-monochrome/SKILL.md   # template skills (30×)
│   └── ...
└── cli/                          # (optional) installer + sync-skills
```

**Kontrak Frontmatter (wajib):**
```yaml
---
name: design-template-<kebab>   # WAJIB sama dengan folder
description: "<vibe> — <1 kalimat>. Use when user wants <trigger words>."
allowed-tools: Read Write Edit Glob Grep
---
```

**Struktur internal (tiap template):**
```md
<role>            # GIMANA agent kerja — audit stack → nanya → plan → code → jelasin
<design-system>   # APA yang agent bangun — Philosophy, Tokens, Components, Layout, Motion, Bold Factor
## How to use this skill
## <Template> Checklist   # Verifikasi sebelum delivery
```

---

## FAQ

**Q: Harus install semua 30 template?**
Gak. Copy *satu* `skills/design-template-*` yang lu butuh. Atau pakai `skills add muris11/design-template --skill design-template-cyberpunk` buat narik satu aja.

**Q: Bakal nimpa tailwind.config gua?**
Gak. Agent *propose* plan dulu (centralize tokens vs adapt). Lu approve. Token disaranin sebagai CSS variables + diff `tailwind.config`, bukan forced overwrite.

**Q: Jalan di luar Claude Code?**
Ya. Agent apapun yang baca `SKILL.md` (OpenCode, Cursor, Windsurf, Copilot) bisa pakai `<role>` + `<design-system>`. Frontmatter `allowed-tools` itu advisory — ignore aja kalau harness lu gak support.

**Q: Konflik nama npm?**
Unscoped `design-template` di npm sudah diambil package `react` lain (v2.0.35). Pakai `muris11-design-template`:
```bash
npm install muris11-design-template
# terus alias kalau mau
ln -s node_modules/muris11-design-template ./design-template
```

**Q: Gimana skills.sh indexing kerja?**
Pas `npm publish`, webhook npm notifikasi skills.sh. Dalam 5-15 menit versi lu muncul di `https://www.skills.sh/muris11/design-template`. Gak perlu `skills publish` manual. Lu juga bisa `npx skills add muris11/design-template` buat force re-index.

**Q: Bisa mix dua template (misal Bauhaus grid + Cyberpunk neon)?**
Jangan. Tiap template palette/radius/shadow-nya sengaja tertutup ("Monochrome is absolute"). Mixing ngerusak vibe. Pilih satu vibe per page/section. Kalau emang butuh hybrid, bikin template *baru* (copy satu, remix token, kasih nama baru).

**Q: License?**
MIT — pakai komersial bebas, atribusi dihargai tapi gak wajib. Lihat [`LICENSE`](./LICENSE).

---

## Versioning & Changelog

Kita pakai **SemVer**: `1.0.x` patch = template baru, `1.x.0` minor = breaking token change, `x.0.0` major = skill contract change.

| Version | Tanggal | Apa |
|---------|---------|-----|
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

Full log: `git log --oneline --graph --all` dan GitHub Releases (tags `v1.0.x`).

---

## Kontribusi

```bash
git clone https://github.com/muris11/design-template.git
cd design-template
# bikin template
Copy-Item -Recurse skills/design-template-monochrome skills/design-template-mybrand
# edit SKILL.md → name + description + <design-system>
npm run sync-skills   # verifikasi name == folder
npm test              # smoke-test load tiap skill
git add . && git commit -m "feat: mybrand v1.0.30" && git push
```

PR welcome — tolong keep satu template per PR, include Checklist, dan keep role utuh.

---

## Kredit & Lisensi

Dibuat oleh [@muris11](https://github.com/muris11) — wrapping **30 identitas desain** dari Swiss grid law sampai vaporwave neon jadi skills yang beneran bisa dipakai agent lu.

Inspirasi desain: Bauhaus, Swiss International, Vogue, Linear, Vercel, Braun / Teenage Engineering, Material You, dan open web.

**Lisensi:** [MIT](./LICENSE) — pakai bebas, keep notice aja.

<p align="center">
  <sub>Kalau <code>design-template</code> ngirit seminggu bikeshedding token lu, kasih ⭐ di <a href="https://github.com/muris11/design-template">GitHub</a> dan <code>skills add</code> di <a href="https://www.skills.sh/muris11/design-template">skills.sh</a> — 5 detik doang dan bikin lampu tetap nyala.</sub>
</p>

<p align="center">
  <img src="images/cover.png" alt="design-template — 30 identitas" width="100%" />
</p>
