# Getting started

DocsForge is a self-contained documentation build system. Everything you need is bundled in the repository — no package manager, no external downloads, no dependency hell.

## Installation

### From GitHub (recommended)

DocsForge is distributed as a GitHub template. The quickest way to start is by forking or cloning the starter repository:

``` bash title="Clone the starter template"
git clone https://github.com/QQSHI13/docsforge-starter.git my-docs
cd my-docs
```

The starter includes:

- The `docsforge` build tool (vendored)
- The Material theme and all its assets (vendored)
- All required Markdown extensions and plugins (vendored)
- A sample `mkdocs.yml` configuration
- A sample `docs/` folder with example content

### Requirements

The only thing you need is **Python 3.8+**. DocsForge bundles everything else.

``` bash title="Check your Python version"
python --version
```

If you don't have Python installed, get it from [python.org](https://python.org) or your system's package manager.

### What's inside?

After cloning, your project looks like this:

``` { .sh .no-copy }
my-docs/
├── docsforge/           # Vendored build tool
│   ├── __init__.py
│   ├── build.py
│   ├── serve.py
│   └── ...
├── material/            # Vendored Material theme
│   ├── templates/
│   ├── assets/
│   └── ...
├── docs/                # Your documentation
│   ├── index.md
│   └── ...
├── mkdocs.yml           # Site configuration
└── README.md
```

All dependencies live inside your project. This means:

- **Reproducible builds**: The same code always produces the same site
- **Offline builds**: No network required once cloned
- **No version conflicts**: Your docs toolchain is isolated per project
- **Easy CI/CD**: Just `git clone` and `python docsforge build`

## Creating your first site

### 1. Configure your site

Open `mkdocs.yml` and customize the basics:

``` yaml title="mkdocs.yml"
site_name: My Project Docs
site_url: https://myproject.github.io/docs/
site_author: Your Name
site_description: Documentation for My Project

repo_name: username/myproject
repo_url: https://github.com/username/myproject
```

### 2. Write your docs

Add Markdown files to the `docs/` directory. The file structure becomes your navigation:

``` { .sh .no-copy }
docs/
├── index.md           # Homepage
├── getting-started.md
├── guides/
│   ├── installation.md
│   └── configuration.md
└── reference/
    └── api.md
```

### 3. Preview locally

Start the development server to see changes as you write:

``` bash
python docsforge serve
```

Visit [localhost:8000](http://localhost:8000). The server auto-reloads when you save changes.

### 4. Build for production

When you're ready to deploy:

``` bash
python docsforge build
```

This creates a `site/` directory with your fully built static site.

## Upgrading DocsForge

Because everything is vendored, upgrading is a `git merge` away:

``` bash title="Add the upstream template as a remote"
git remote add upstream https://github.com/QQSHI13/docsforge-starter.git
git fetch upstream
```

``` bash title="Merge updates into your project"
git merge upstream/main --no-commit
# Review changes, then commit
git commit -m "Update docsforge to latest"
```

You control when to upgrade. No surprise breaking changes from external package updates.

## Need help?

- Browse the [Setup Guides](setup/index.md) for customization options
- Check the [Reference](reference/index.md) for Markdown syntax
- See [Publishing](publishing-your-site.md) for deployment options
