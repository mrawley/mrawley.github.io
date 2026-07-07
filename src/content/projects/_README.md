# Content collection placeholder

Markdown files in this folder become entries in the `projects` content collection.

Each file frontmatter must match the schema in `src/content.config.ts`:

```yaml
---
title: "Project name"
description: "One-line description"
year: 2026            # number or string
role: "PM"            # optional
stack: ["Astro", "GitHub Pages"]  # optional array
link: "https://..."   # optional URL
repo: "https://..."   # optional URL
featured: false       # default false
order: 100            # default 100 (lower = shown first)
type: "personal"      # "work" | "personal", default "personal"
---

Body content in markdown. Rendered only on individual project pages if one exists.
```

**Do not commit this file to production content**. It exists so the folder stays in git; delete once real projects live here.
