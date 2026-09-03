# Contributing to `design-template`

> Terima kasih cuy mau kontribusi! Repo ini isinya 30+ design identities sebagai agent skills. Satu skill = satu vibe yang konsisten. Kontribusi paling berharga adalah **template baru**.

## Cara Paling Cepat — Template Baru (5 menit)

```powershell
# 1. Copy template terdekat sebagai starter
Copy-Item -Recurse skills/design-template-monochrome skills/design-template-mybrand

# 2. Edit SKILL.md — WAJIB ganti 2 hal:
#    - frontmatter `name:` HARUS sama dengan nama folder
#    - `description:` tambah trigger words (kapan skill ini ke-load)
---
name: design-template-mybrand
description: "MyBrand — warm terracotta + cream, Canela serif, arch 200px. Use when user wants mybrand, terracotta, warm editorial."
allowed-tools: Read Write Edit Glob Grep
---

# 3. Ganti isi <design-system>
#    - Tokens (colors, typography, radius, shadows)
#    - Components (buttons, cards, inputs)
#    - Layout, Motion, Bold Factor
#    - Checklist di akhir (wajib ada, agent cek ini sebelum ship)

# 4. Daftarin di router & loader (biar ke-detect)
#    - Tambah 1 baris di skills/design-template/SKILL.md (tabel)
#    - Tambah 1 baris di skills/design-template-all/SKILL.md (Steps: 1.)

# 5. Bump version + push
#    package.json + .claude-plugin/plugin.json → 1.0.x → 1.0.(x+1)
git add .
git commit -m "feat: mybrand v1.0.30"
git tag v1.0.30
git push origin main --tags
```

## Aturan Main

1. **`name` == folder** — kalau beda, skill gak ke-load di `skill` tool.
2. **Satu vibe = satu skill** — jangan campur token Monochrome (`#000/#FFF`) sama Bauhaus (`#D02020/#1040C0`). Mixing ngerusak identitas.
3. **Keep `<role>`** — audit stack → nanya scope → bikin plan → nulis kode → jelasin kenapa. Ini yang jamin output stack-idiomatic.
4. **Checklist wajib** — tiap template diakhiri `## <Name> Checklist` — agent cek ini sebelum delivery.
5. **Satu template per PR** — biar review gampang. Include checklist & trigger words.

## Dev Setup

```bash
git clone https://github.com/muris11/design-template.git
cd design-template
npm install
npm run sync-skills   # verifikasi name == folder untuk 32 skills
npm test              # smoke-test load tiap SKILL.md via skill tool
npm pack --dry-run    # cek 40 files, 1.7MB, scoped @muris11/design-template
```

## Commit Convention

- `feat: <template> v1.0.x` — template baru
- `fix: ...` — bug token / typo
- `docs: ...` — README / docs
- `chore: bump 1.0.x → 1.0.y` — version only

## Code of Conduct

Be kind. Jaga vibe. Kalau mau diskusi template baru, buka **Issue** dulu dengan label `new-template` — kita brainstorm bareng sebelum lu nulis 800 baris spec.

## License

By contributing, you agree your contributions will be licensed under the same **MIT License**.

---

Butuh bantuan? Buka Issue atau tag `@muris11` di Discussion. Gass 🚀
