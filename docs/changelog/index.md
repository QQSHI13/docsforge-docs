# Changelog

All notable changes to DocsForge are documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [10.1.0] — 2026-05-10

### Added

- **Zero-config Markdown** — 31 extensions loaded by default (all pymdownx + python-markdown). No `markdown_extensions:` config needed.
- **KaTeX math** — Vendored KaTeX (1.5MB) renders `$$...$$` inline and display math. No CDN, no config.
- **Pygments highlighting** — Syntax-colored code blocks at build time. No client-side JS.
- **Dark mode toggle** — Light/dark mode switch in header. Auto-detects system preference.
- **Auto-loaded plugins** — search, tags, blog, info, meta, minify, privacy all work without config.
- **Self-hosted fonts** — Privacy plugin downloads and caches Google Fonts locally.

### Changed

- **Config file** renamed from `properdocs.yml` to `docsforge.yml`
- **Theme namespace** changed from `mkdocs.themes` to `docsforge.themes`
- **Plugin system** — 6 plugins removed, 7 remain as built-in defaults

### Removed

- `typeset` — Users can write Unicode directly
- `optimize` — Requires external `pngquant` binary
- `social` — Requires Pillow + CairoSVG
- `projects` — Niche multi-project feature
- `offline` — Privacy plugin covers most use cases
- `group` — Plugin orchestrator (niche)

## [0.1.0] — 2025-05-10

### Added

- Initial release
