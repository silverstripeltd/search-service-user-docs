# Documentation conventions

This repository contains user documentation for Silverstripe Search, located under `docs/en/`.

These docs follow the [Silverstripe documentation conventions](https://docs.silverstripe.org/en/contributing/documentation/) and are rendered by a system that understands the numbered-prefix directory structure (e.g. `01_Getting_started/`, `02_Features/`).

## Links

### Internal links

- Use **absolute paths from the docs root**, without `.md` extensions:
  - `[Features](/features)` — links to `02_Features/index.md`
  - `[Developer's guide](/developers-guide)` — links to `03_developers-guide.md`
  - `[Engines and Schema](/features/engines-and-schema)` — links to `02_Features/01_engines-and-schema.md`
- The numbered prefixes (e.g. `01_`, `02_`) are **stripped** in URLs; use the plain name.
- Underscores in folder names become underscores in the URL (e.g. `04_Security_guide` → `/security_guide`).
- For anchors, append `#section-name`: `[Schema](/features/engines-and-schema#schema)`
- Relative links (e.g. `../documents-and-files`) are acceptable for sibling pages within the same section.

### What NOT to do

- **No `.md` extensions** in internal links — use `/features/search` not `/features/search.md`
- **No Pelican-style links** — do not use `{filename}` or `{static}` prefixes (e.g. `{filename}/pages/features.md`). These are from an old build system.
- External links (e.g. to GitHub repos) **do** keep their full URL including `.md` if needed.

## Formatting

### Alerts / callouts

Use GitHub-style alert syntax, not HTML `<div class="callout">` blocks:

```markdown
> [!NOTE]
> This is a note.
```

Map old callout levels: `callout-info` → `[!NOTE]`

### Inline code

- Use markdown backticks `` `code` `` for inline code in regular markdown content.
- `<code></code>` tags are acceptable **only inside HTML blocks** (e.g. within `<table>` or `<td>` elements) where markdown backticks won't render.

### Frontmatter

Pages use YAML frontmatter with `title` and optionally `summary` and `introduction`:

```yaml
---
title: Page Title
summary: Short description
introduction: Longer introduction text
---
```
