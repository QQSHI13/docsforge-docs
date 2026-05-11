# Getting started

DocsForge is a self-contained documentation engine. `pip install`, write Markdown, build.

## Installation

```bash
pip install docsforge
```

Requires **Python 3.10+**.

## Quick start

```bash
# Create a new project
docsforge new my-docs
cd my-docs

# Start the dev server
docsforge serve

# Build for production
docsforge build
```

## What's inside

After `docsforge new`, your project looks like this:

``` { .sh .no-copy }
my-docs/
├── docsforge.yml    # Site configuration
├── docs/
│   └── index.md     # Homepage
└── site/            # Build output
```

## Configuration

The smallest valid `docsforge.yml`:

```yaml
site_name: My Project
```

That's it. All plugins, extensions, and theme settings use sensible defaults. Add configuration only when you need to customize.

## Key defaults

| Feature | Default |
|---------|---------|
| Theme | Material (built-in) |
| Plugins | search, tags, blog, info, meta, minify, privacy |
| Markdown extensions | 31 total — all pymdownx + python-markdown |
| Math | KaTeX (vendored, `$$...$$` works) |
| Code highlighting | Pygments (colored syntax) |
| Dark mode | Light/dark toggle in header |
| Fonts | Self-hosted (privacy plugin downloads Google Fonts) |

## Next steps

- [Creating your site](creating-your-site.md)
- [Reference](reference/index.md)
