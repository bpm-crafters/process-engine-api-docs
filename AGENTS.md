# AGENTS.md

## 1. Overview

This repository publishes the Process Engine API documentation site. It explains the engine-independent API and its supporting components and adapters.

## 2. Folder Structure

- `docs`: source content and assets for the published MkDocs site.
  - `introduction`: motivation, architecture, and component-overview pages.
  - `getting-started`: introductory integration guidance and examples.
  - `reference-guide`: local reference-guide entry points; detailed API and adapter pages are imported from related repositories.
  - `developer-guide`: contribution and local documentation-build guidance.
  - `assets/img`: site imagery and editable Draw.io source diagrams.
  - `stylesheets`: Material theme overrides.
  - `requirements.txt`: Python dependencies used to build the site.
- `mkdocs.yml`: site metadata, Material configuration, plugins, imported repositories, and navigation; keep it aligned with files and links in `docs`.
- `.editorconfig`: shared whitespace, encoding, line-ending, and line-length rules.
- `README.md`: concise project description and public documentation link.

## 3. Core Behaviors & Patterns

- Markdown files under `docs` are the local source of truth; MkDocs turns them into the static site.
- `mkdocs.yml` imports selected Markdown (and image assets where needed) from the Process Engine API, worker, and adapter repositories. Navigation may therefore reference paths outside this checkout.
- Pages use YAML front matter where page metadata is needed, standard Markdown headings, fenced language-tagged code examples, and MkDocs admonitions such as `!!! note` and `!!! warning`.
- Keep navigation paths and relative links valid under `use_directory_urls: false`.
- Maintain editable `.drawio` files alongside their rendered PNG diagrams when changing diagrams.
- Keep CSS customizations in `docs/stylesheets/extra.css`; preserve the existing Material theme selector structure and CSS custom-property approach.

## 4. Conventions

- Write documentation in English with concise, reader-focused prose; retain established Process Engine API terminology and API identifiers.
- Use sentence-style Markdown headings and descriptive link text. Use backticks for filenames, configuration keys, commands, APIs, and artifact coordinates.
- Use fenced code blocks with an appropriate language (`bash`, `xml`, `java`, and so on); do not alter their contents when editing surrounding prose.
- Follow `.editorconfig`: UTF-8, LF line endings, two-space indentation, final newline, and a 160-character maximum line length. Markdown may intentionally retain trailing spaces.
- Update `mkdocs.yml` whenever adding, moving, or removing a page that belongs in the published navigation.

## 5. Working Agreements

- Respond in English; keep technical terms in English and never translate fenced code blocks.
- Create tests, lint tasks, or formatting tasks only when explicitly requested.
- Before editing, review related usages, navigation, and recurring patterns.
- Prefer simple, focused changes; do not add features or abstractions beyond the request.
- Ask for clarification when requirements are materially ambiguous.
- Keep changes minimal. Add comments only for non-obvious logic or invariants.
- New content should be focused and located beside related documentation.
- Do not add speculative fallbacks, compatibility shims, or legacy branches unless explicitly requested; prefer clear failures over silent fallback behavior.
