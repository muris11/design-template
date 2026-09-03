---
name: design-template
description: "Core router for design-template. Use to list available templates or when user says 'design-template' without specifying sub-template. Routes to monochrome etc."
allowed-tools: Read Write Edit Glob Grep
---
# design-template (core router)

> Core entry for `design-template` skill family. Tiap visual identity adalah sub-skill terpisah.

## Available templates

| Skill | Trigger words | Vibe |
|-------|---------------|------|
| `design-template-monochrome` | monochrome, black white, editorial, luxury, stark, serif minimal, pure bw | Austere, editorial luxury — pure #000/#FFF, serif hero, 0px radius, inversion |

## How to use

- User nyebut template spesifik (misal "pakai monochrome") → load `design-template-monochrome` langsung, jangan load core ini.
- User cuma bilang "design-template" atau "kasih template" → list tabel di atas, tanya mau yang mana.
- User mau bikin template baru → `Copy-Item skills/design-template-monochrome skills/design-template-<nama>` lalu ganti isi `<design-system>`.

## Next templates (placeholder)

- `design-template-brutalist` — industrial raw
- `design-template-minimal-modern` — blue accent sans
- Tambah sesuai kebutuhan, ikuti pola folder + frontmatter `name` = nama folder.
