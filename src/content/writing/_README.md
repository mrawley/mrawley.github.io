# Content collection placeholder

Markdown files in this folder become entries in the `writing` content collection.

Each file frontmatter must match the schema in `src/content.config.ts`:

```yaml
---
title: "Post title"
description: "One-line summary shown on the writing index"
pubDate: 2026-07-06         # ISO date
updatedDate: 2026-07-10     # optional ISO date
tags: ["tag1", "tag2"]      # optional array
draft: false                # default false; if true, hidden from list + build
featured: false             # default false
---

Post body in markdown.
```

**Do not commit this file to production content**. It exists so the folder stays in git; delete once real writing lives here.
