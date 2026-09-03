---
name: design-template-all
description: "One-shot loader for full design-template family. Invoke when user says 'design-template semua' or wants all templates at once."
---

# design-template-all

Load ALL design-template skills at once, then follow them for rest of session.

## Steps

1. Invoke each skill via skill tool, in order:
   - `design-template` (core router)
   - `design-template-monochrome` (Minimalist Monochrome)

2. Follow the loaded design system's role + tokens. If multiple templates loaded, ask user which template to apply (don't mix tokens).

3. If any skill fails to load/missing, report which one, continue with rest.
