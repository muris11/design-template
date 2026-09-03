# design-template

> Kumpulan design system sebagai agent skills. Tiap sub-skill = satu identitas visual lengkap. Contoh: `design-template-monochrome`.

## Struktur

```
design-template/
├── design-template.md                    # core router + daftar template
├── plugin.json / package.json / .claude-plugin/plugin.json
├── rules/
└── skills/
    ├── design-template/SKILL.md          # core router (list template)
    ├── design-template-monochrome/SKILL.md # Minimalist Monochrome (role + tokens lengkap)
    ├── design-template-all/SKILL.md      # loader all-in-one
    └── design-template-<nama>/SKILL.md   # next templates (copy monochrome)
```

## Pakai

- **Monochrome**: load `design-template-monochrome` → agent langsung dapat role + pure B&W tokens (#000/#FFF, serif Playfair, 0px radius, inversion).
- **Semua**: load `design-template-all`
- **List**: load `design-template` core

## Tambah template baru (30 detik)

```powershell
Copy-Item -Recurse skills/design-template-monochrome skills/design-template-brutalist
# edit skills/design-template-brutalist/SKILL.md:
# - ganti name: design-template-brutalist
# - ganti description trigger words
# - ganti isi <design-system> (tokens, components, motion)
# tambah baris di skills/design-template/SKILL.md tabel + skills/design-template-all/SKILL.md loader
```

Template `monochrome` adalah contoh lengkap (role + 700 baris design-system + checklist). Copy polanya buat `brutalist`, `minimal-modern`, `neon`, dll.

## Aturan
- `name` frontmatter HARUS sama dengan nama folder
- Jangan campur tokens antar template
- Satu template = satu vibe yang konsisten sampai ke texture & motion
