# design-template — Core

> Kumpulan design system sebagai agent skills. Tiap sub-skill = satu identitas visual lengkap (tokens, components, motion, layout).

## Cara pakai

1. User pilih template: `design-template-monochrome` (atau template lain yang akan lu tambah)
2. Agent load skill tersebut → otomatis dapat `<role>` + `<design-system>` lengkap di context
3. Agent ikuti role dulu (audit stack → tanya scope → plan) baru nulis code sesuai design tokens

## Daftar template

| Skill | Vibe | Kapan pakai |
|-------|------|-------------|
| `design-template-monochrome` | Pure B&W, serif editorial, sharp 0px, inverted stats | Luxury, fashion, gallery, monograph, high-contrast editorial |
| *(next)* `design-template-brutalist` | *(contoh next)* | Industrial, raw |
| *(next)* `design-template-minimal-modern` | Blue accent + Inter | Tech SaaS |

## Nambah template baru

```powershell
Copy-Item -Recurse skills/design-template-monochrome skills/design-template-<nama-baru>
# edit SKILL.md → ganti name, description, dan isi <design-system>
# tambah baris di skills/design-template-all/SKILL.md loader
# tambah baris di tabel atas
```

## Aturan
- Satu template = satu folder skill, `name` frontmatter HARUS sama dengan nama folder
- Jangan campur tokens antar template. Monochrome = #000/#FFF only, no accent.
- Semua template inherit role yang sama (audit stack → tanya scope → plan → code), cuma design-system yang beda.
