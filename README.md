# Search service user docs

The user documentation for [Silverstripe Search](https://github.com/silverstripeltd) - a user-focused reference for the editors and administrators who create and manage search, plus a developer's guide. The published site covers version 1.x of the service.

## Structure

All content lives under `docs/en/`, organised with numbered-prefix directories that set the order of the site:

- `01_Getting_started/`
- `02_Features/`
- `03_developers-guide.md`
- `04_Security_guide/`
- `05_faq.md`
- `06_Changelogs/`
- `07_glossary.md`

The numbered prefixes are stripped from the published URLs (e.g. `02_Features/01_engines-and-schema.md` is served at `/features/engines-and-schema`).

## Conventions

These docs follow the [Silverstripe documentation conventions](https://docs.silverstripe.org/en/contributing/documentation/). In short:

- Each page has YAML frontmatter with a `title` (and optional `summary` / `introduction`).
- Internal links use absolute paths from the docs root, without `.md` extensions (e.g. `[Features](/features)`).
- Callouts use GitHub-style alerts (`> [!NOTE]`).
- NZ/British English spelling.

## Editing and previewing

Edit the Markdown under `docs/en/` directly. There is no local build step - the published site is rebuilt automatically when changes land on the `2` branch (a Netlify build hook, see `.github/workflows/build-deploy.yml`). Preview changes by reading the Markdown and checking that links resolve.
