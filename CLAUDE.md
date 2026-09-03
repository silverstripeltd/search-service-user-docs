# Search user docs

User documentation for Silverstripe Search, under `docs/en/`. Rendered to a docs site (Netlify) by a system that understands the numbered-prefix directory structure (`01_Getting_started/`, `02_Features/`, ...). Follows the [Silverstripe documentation conventions](https://docs.silverstripe.org/en/contributing/documentation/). The near-total activity here is writing and editing docs; the conventions below are the priority.

These conventions apply to content you are adding or changing. Do not retrofit existing pages to match unless explicitly asked.

## Audience and tone

- Written for the people who use Silverstripe Search - editors and administrators - plus a developer audience in the developer's guide. Assume a non-specialist reader for most pages.
- Friendly, clear, and professional. Address the reader directly ("your content", "you can..."). Explain capabilities and outcomes, not internals.
- **NZ/British English spelling** (`customise`, `organisation`, `behaviour`).
- Lead a section with what it is for and who it helps before diving into detail.

## Page structure

- Numbered-prefix directories order the site (`01_`, `02_`, ...); the prefixes are stripped from URLs.
- Every page has YAML frontmatter: `title` (required), optional `summary` and `introduction`.
- Use `##` and `###` headings within a page (the H1 comes from `title`). Keep headings task- or feature-oriented.

## Links

- Use **absolute paths from the docs root, without `.md`**: `[Features](/features)`, `[Engines and Schema](/features/engines-and-schema)`.
- Numbered prefixes are **stripped** in URLs (`02_Features/01_engines-and-schema.md` -> `/features/engines-and-schema`). Underscores in folder names stay (`04_Security_guide` -> `/security_guide`).
- Anchors: append `#section-name`. Relative links to sibling pages within a section (e.g. `../documents-and-files`) are acceptable.
- **Do not** add `.md` extensions to internal links. **Do not** use Pelican-style `{filename}` / `{static}` prefixes - those are from an old build system. External links keep their full URL (including `.md` if needed).

## Formatting

- **Callouts:** use GitHub-style alerts, not `<div class="callout">`. Map `callout-info` -> `[!NOTE]`.
  ```markdown
  > [!NOTE]
  > This is a note.
  ```
- **Tables:** complex tables are written as raw HTML with Bootstrap classes (`<table class="table table-hover table-bordered">`), since markdown tables can't carry the styling. Simple tables can use markdown.
- **Inline code:** markdown backticks in normal content. `<code></code>` only inside HTML blocks (e.g. tables) where backticks won't render.

## Build

There is no local build. Pushing to the `2` branch triggers a Netlify build hook (`.github/workflows/build-deploy.yml`) - there are no local test/lint/build commands. Validate changes by reading the Markdown and checking that links resolve and headings/frontmatter are well-formed.
