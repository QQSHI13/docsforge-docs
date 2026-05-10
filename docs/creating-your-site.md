# Creating your site

After you've [installed](getting-started.md) DocsForge, it's time to build your documentation. This guide walks through project structure, configuration, and writing your first pages.

## Project structure

A DocsForge project is simple:

``` { .sh .no-copy }
my-docs/
├── docsforge/           # Vendored build system (don't touch)
├── material/            # Vendored theme (don't touch)
├── docs/                # Your documentation files
│   └── ...
├── mkdocs.yml           # Site configuration
└── README.md
```

### The `docs/` directory

This is where your content lives. Every Markdown file (`.md`) becomes a page. Subdirectories become sections in the navigation.

``` { .sh .no-copy }
docs/
├── index.md              # Landing page (required)
├── getting-started.md    # Top-level page
├── guides/
│   ├── index.md          # Section landing page
│   ├── install.md
│   └── configure.md
└── reference/
    ├── index.md
    └── api.md
```

### The `mkdocs.yml` file

This configures your entire site. DocsForge uses standard MkDocs configuration with Material-specific extensions.

## Configuration

### Minimal configuration

The smallest valid `mkdocs.yml`:

``` yaml
site_name: My Project
site_url: https://example.com/docs/
```

### Recommended configuration

``` yaml title="mkdocs.yml"
site_name: My Project Documentation
site_url: https://myproject.github.io/docs/
site_author: Your Name
site_description: >-
  Complete documentation for My Project

repo_name: username/myproject
repo_url: https://github.com/username/myproject

copyright: Copyright &copy; 2025 Your Name

theme:
  name: material
  features:
    - navigation.tabs
    - navigation.sections
    - navigation.top
    - search.highlight
    - search.suggest
    - content.code.copy
  palette:
    - media: "(prefers-color-scheme: light)"
      scheme: default
      primary: teal
      accent: teal
      toggle:
        icon: material/brightness-7
        name: Switch to dark mode
    - media: "(prefers-color-scheme: dark)"
      scheme: slate
      primary: black
      accent: teal
      toggle:
        icon: material/brightness-4
        name: Switch to light mode

plugins:
  - search
  - minify:
      minify_html: true

markdown_extensions:
  - admonition
  - attr_list
  - pymdownx.highlight
  - pymdownx.superfences
  - pymdownx.tabbed:
      alternate_style: true
```

### Customizing the navigation

By default, DocsForge builds navigation from your `docs/` directory structure. You can also define it explicitly in `mkdocs.yml`:

``` yaml
nav:
  - Home: index.md
  - Getting Started:
    - Installation: getting-started.md
    - Configuration: configuration.md
  - Guides:
    - guides/index.md
    - Installation: guides/install.md
    - Configuration: guides/configure.md
  - Reference:
    - reference/index.md
    - API: reference/api.md
```

## Writing content

DocsForge supports standard Markdown plus powerful extensions. Here's a quick taste:

### Admonitions

``` markdown
!!! note "Important note"
    This is a note callout box.
```

!!! note "Important note"
    This is a note callout box.

### Code blocks with titles

``` python title="hello.py"
def greet(name):
    print(f"Hello, {name}!")
```

### Content tabs

``` markdown
=== "Linux"
    ``` bash
    python docsforge serve
    ```

=== "Windows"
    ``` powershell
    python docsforge serve
    ```
```

=== "Linux"
    ``` bash
    python docsforge serve
    ```

=== "Windows"
    ``` powershell
    python docsforge serve
    ```

See the [Reference](reference/index.md) section for the full syntax guide.

## Previewing as you write

Start the development server:

``` bash
python docsforge serve --livereload
```

Visit [localhost:8000](http://localhost:8000). Changes are rebuilt automatically as you save.

!!! tip

    For large documentation projects, use the `--dirtyreload` flag to only rebuild changed pages:
    
    ``` bash
    python docsforge serve --dirtyreload
    ```

## Building your site

When you're ready to publish:

``` bash
python docsforge build
```

This creates a `site/` directory containing your fully built static site. Upload these files to any web host, CDN, or static site platform.

## Next steps

- [Publishing your site](publishing-your-site.md) — Deploy to GitHub Pages, Netlify, Vercel, or any host
- [Setup guides](setup/index.md) — Customize colors, fonts, navigation, and more
- [Reference](reference/index.md) — Full Markdown syntax guide
