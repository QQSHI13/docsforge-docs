# Philosophy

DocsForge exists because we believe documentation tooling should be **simple, transparent, and reliable**.

## The problem with modern docs tooling

Documentation tools have become increasingly complex. What started as "write Markdown, get a website" now involves:

- Package managers with dependency resolution
- Node.js version conflicts and `node_modules` bloat
- Build pipelines that break when a transitive dependency updates
- CI/CD environments that need special caching configuration
- Toolchains that don't work without internet access

We've all been there: you return to a documentation project after six months, run the build command, and it fails because some package somewhere updated and broke compatibility. You spend an hour fixing the toolchain instead of writing documentation.

## Our principles

### 1. Self-containment

**Everything needed to build your docs should be in your repository.**

DocsForge vendors all dependencies — the build tool, the theme, the extensions, the icon fonts. When you clone a DocsForge project, you have everything. No `pip install`, no `npm install`, no downloads at build time.

This means:
- Your documentation builds in 10 years exactly as it does today
- You can build on a plane, in a submarine, or behind a corporate firewall
- Your CI/CD pipeline is `git clone` → `python docsforge build`
- You never waste time debugging dependency conflicts

### 2. Explicit over implicit

**You should know exactly what code builds your site.**

When you use DocsForge, all the code is right there in your repo. You can read it, modify it, fork it. There are no hidden transitive dependencies three layers deep that might change behavior or introduce vulnerabilities.

### 3. Defaults that delight

**You shouldn't need to configure 50 things before your site looks good.**

DocsForge ships with carefully chosen defaults:
- A professional Material Design theme
- Responsive layout that works on all devices
- Light and dark mode with system preference detection
- Search, navigation, and code highlighting enabled by default
- Typography and spacing tuned for readability

Start writing immediately. Customize when you're ready.

### 4. Markdown is enough

**Your content should be in Markdown, not in proprietary formats or JavaScript code.**

DocsForge extends standard Markdown with useful syntax (admonitions, tabs, code blocks), but everything is still plain text. Your documentation remains:
- Readable in any text editor
- Diff-friendly in version control
- Portable to any other Markdown-based tool
- Accessible to contributors who don't know your toolchain

### 5. Documentation should outlive its toolchain

**The tool you use to build docs should not be a liability.**

When you choose a documentation platform, you're making a bet. Will it still exist in 5 years? Will it change pricing? Will it get acquired and shut down?

DocsForge mitigates this risk:
- Everything is open source (MIT license)
- Everything is in your repository (no external lock-in)
- The underlying format is standard Markdown (universally portable)
- You control when and how to update

## Who DocsForge is for

DocsForge is designed for:

- **Open source projects** that want professional docs without CI complexity
- **Enterprise teams** working in air-gapped or heavily regulated environments
- **Individual developers** who value simplicity and reliability
- **Technical writers** who want to focus on content, not tooling
- **Anyone** who has ever said "it worked yesterday" about a documentation build

## Who DocsForge is not for

DocsForge might not be the right choice if you need:

- **Server-side features** — DocsForge builds static sites. No server-side rendering, no APIs, no dynamic content.
- **Real-time collaboration** — Use Google Docs, Notion, or Confluence for collaborative drafting. Export to DocsForge for publishing.
- **Complex authentication** — Static sites are public by default. Use your hosting platform's auth features if needed.

## Inspirations

DocsForge stands on the shoulders of excellent open source projects:

- [MkDocs](https://www.mkdocs.org) — The static site generator that powers everything
- [Material for MkDocs](https://squidfunk.github.io/mkdocs-material/) — The beautiful theme we bundle
- [Python Markdown](https://python-markdown.github.io/) — The Markdown parser
- [Pymdown Extensions](https://facelessuser.github.io/pymdown-extensions/) — The Markdown extensions

We're grateful to the maintainers and contributors of these projects. DocsForge's contribution is packaging them into a self-contained, zero-config distribution.

## License

DocsForge is released under the MIT License. The vendored components retain their original licenses (all permissive open source licenses).

See [License](license.md) for full details.
