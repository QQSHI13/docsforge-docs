# Features

DocsForge combines the best of modern documentation tooling into a single, self-contained package. Here's what you get out of the box.

## Core Features

<div class="grid cards" markdown>

-   :material-package-variant-closed:{ .lg .middle } &nbsp; **Self-Contained Builds**

    ---

    Every dependency is vendored into your project. No network calls during build. No surprise dependency updates. Reproducible builds, guaranteed.

-   :material-rocket-launch:{ .lg .middle } &nbsp; **Zero Configuration**

    ---

    Start with a working site in seconds. Sensible defaults for theme, navigation, search, and styling. Customize only what you need.

-   :material-theme-light-dark:{ .lg .middle } &nbsp; **Light & Dark Mode**

    ---

    Automatic system preference detection with a manual toggle. Both modes are fully customizable with your brand colors.

-   :material-magnify:{ .lg .middle } &nbsp; **Full-Text Search**

    ---

    Client-side search with instant results, highlighting, suggestions, and keyboard shortcuts. No external service required.

-   :material-responsive:{ .lg .middle } &nbsp; **Responsive Design**

    ---

    Looks great on every device — phones, tablets, laptops, and widescreen monitors. Touch-friendly navigation.

-   :material-image:{ .lg .middle } &nbsp; **Social Cards**

    ---

    Automatic Open Graph and Twitter Card generation for rich link previews when your docs are shared.

</div>

## Content Features

### Rich Markdown

DocsForge extends standard Markdown with powerful syntax for technical writing:

- **Admonitions** — Note, warning, tip, danger, and custom callout boxes
- **Code blocks** — Syntax highlighting for 300+ languages, line numbers, annotations, copy-to-clipboard
- **Content tabs** — Group related content with tabbed interfaces
- **Data tables** — Sortable, styled tables with column alignment
- **Diagrams** — Mermaid.js integration for flowcharts, sequence diagrams, and more
- **Math** — LaTeX rendering with MathJax or KaTeX
- **Icons and emojis** — 8,000+ icons and 3,000+ emojis via `:material-heart:` syntax

### Navigation

- **Tabbed sections** — Top-level sections become tabs
- **Section indexes** — Click a section header to see its landing page
- **Breadcrumbs** — Track your location in the page hierarchy
- **Table of contents** — Auto-generated, sticky sidebar with deep linking
- **Footer navigation** — Previous/next page links at the bottom of every page

### Search

- **Instant results** — Search as you type
- **Highlighting** — Matching terms highlighted in results
- **Suggestions** — Autocomplete with keyboard navigation
- **Sharing** — Copy a direct link to any search result
- **Stemming** — Finds "run" when you search for "running"

## Build Features

### Optimization

- **HTML minification** — Strips whitespace and comments from output
- **Asset compression** — Gzip-compatible static assets
- **Incremental builds** — Only rebuild changed pages during development

### Integration

- **Git repository links** — "Edit this page" and "View source" buttons
- **Git revision date** — Show when each page was last updated
- **Analytics** — Plausible, Google Analytics, or custom providers
- **Comments** — Giscus (GitHub Discussions) or Disqus integration

## What DocsForge Includes (Vendored)

| Component | Version | Purpose |
|-----------|---------|---------|
| MkDocs | latest | Static site generator |
| Material theme | latest | Professional theme |
| Pygments | latest | Syntax highlighting |
| Python Markdown | latest | Markdown parser |
| Pymdown Extensions | latest | Markdown extensions |
| Lunr.js | latest | Client-side search |
| Mermaid.js | latest | Diagram rendering |
| Material icons | latest | 8,000+ vector icons |
| Twemoji | latest | Emoji SVG fallback |

All components are vendored as part of the starter template. You control when to update.

## Philosophy

DocsForge believes that:

1. **Documentation should be easy to maintain** — If updating your docs toolchain is harder than writing docs, the toolchain is wrong.

2. **Dependencies should be explicit** — You should know exactly what code builds your site. No hidden transitive dependencies.

3. **Builds should be reproducible** — The same commit should always produce the same site. No "works on my machine."

4. **Documentation should work offline** — Your docs build pipeline should work on a plane, in a submarine, or in a corporate air-gap.

## Comparison with other tools

| Feature | DocsForge | MkDocs + Material | Docusaurus | GitBook |
|---------|-----------|-------------------|------------|---------|
| Self-contained | :material-check: | :material-close: | :material-close: | :material-close: |
| No install step | :material-check: | :material-close: | :material-close: | N/A (SaaS) |
| Material Design | :material-check: | :material-check: | :material-close: | :material-close: |
| Client-side search | :material-check: | :material-check: | :material-check: | :material-close: |
| Offline builds | :material-check: | :material-close: | :material-close: | :material-close: |
| Open source | :material-check: | :material-check: | :material-check: | :material-close: |
| Free hosting | :material-check: | :material-check: | :material-check: | :material-close: |

## Next steps

- [Getting Started](getting-started.md) — Install DocsForge and create your first site
- [Setup Guides](setup/index.md) — Customize every aspect of your documentation
- [Reference](reference/index.md) — Master the Markdown syntax
