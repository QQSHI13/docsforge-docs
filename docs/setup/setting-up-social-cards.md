# Setting up social cards

Social cards (Open Graph and Twitter Cards) create rich link previews when your documentation is shared on social media, messaging apps, or Slack.

## What are social cards?

When someone shares a link to your docs, the platform fetches metadata to generate a preview card with:
- Title
- Description
- Image
- Site name

Example of a rich preview:

```
┌─────────────────────────────┐
│ My Project Documentation    │
│ Learn how to build amazing   │
│ things with our API...       │
│                             │
│    [preview image]          │
│                             │
│ docs.example.com            │
└─────────────────────────────┘
```

## Basic configuration

DocsForge generates social card metadata automatically from your page content. Configure the site-wide defaults:

``` yaml
site_name: My Project Docs
site_description: Complete documentation for My Project
site_url: https://docs.example.com/
```

## Customizing per page

Override social card data for individual pages using front matter:

``` yaml
---
social:
  cards_layout_options:
    title: Custom title for this page
    description: Custom description
---
```

## Open Graph tags

DocsForge automatically generates these Open Graph tags:

- `og:title` — Page title
- `og:description` — Page description or site description
- `og:type` — `website`
- `og:url` — Canonical page URL
- `og:image` — Social card image (if generated)
- `og:site_name` — Site name

## Twitter Cards

Twitter/X uses similar metadata:

- `twitter:card` — `summary_large_image`
- `twitter:title` — Page title
- `twitter:description` — Page description
- `twitter:image` — Card image

## Verifying your cards

Test your social cards with these tools:

- [Twitter Card Validator](https://cards-dev.twitter.com/validator)
- [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/)
- [LinkedIn Post Inspector](https://www.linkedin.com/post-inspector/)

## Troubleshooting

### Cards not appearing

1. Ensure `site_url` is set correctly in `mkdocs.yml`
2. Your site must be publicly accessible (validators can't reach localhost)
3. Platforms cache metadata — use the debugger tools to force a refresh

### Wrong image or description

1. Check page front matter for `social` overrides
2. Ensure `site_description` is set in `mkdocs.yml`
3. First paragraph of each page is used as fallback description

## Next steps

- [Building an optimized site](building-an-optimized-site.md)
- [Adding a git repository](adding-a-git-repository.md)
