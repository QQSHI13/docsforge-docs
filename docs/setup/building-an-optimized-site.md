# Building an optimized site

DocsForge includes tools to optimize your built site for performance and size.

## HTML minification

Enable HTML minification to reduce file sizes:

``` yaml
plugins:
  - minify:
      minify_html: true
```

This strips:
- Whitespace and newlines
- HTML comments
- Optional attribute quotes

## Image optimization

Before adding images to your docs, optimize them:

``` bash
# Using pngquant for PNGs
pngquant --quality=70-90 docs/assets/images/*.png

# Using cwebp for WebP conversion
cwebp -q 80 image.png -o image.webp
```

## Lazy loading

Images load lazily by default in modern browsers. DocsForge adds the `loading="lazy"` attribute automatically.

## Fonts

Use `font: false` if you don't need custom fonts (falls back to system fonts):

``` yaml
theme:
  font: false
```

This removes all Google Fonts requests.

## Search index size

For very large documentation sites, the search index can become large. Consider:

- Excluding less important pages with `search.exclude`
- Splitting documentation into multiple sites

## Complete optimization example

``` yaml
plugins:
  - search
  - minify:
      minify_html: true

theme:
  font:
    text: Roboto  # Only load fonts you need
    code: Roboto Mono
```

## Performance checklist

Before publishing:

- [ ] Enable `minify` plugin
- [ ] Optimize all images
- [ ] Consider if custom fonts are necessary
- [ ] Test with browser DevTools Network tab
- [ ] Check Lighthouse score

## Next steps

- [Adding a git repository](adding-a-git-repository.md)
- [Publishing your site](../publishing-your-site.md)
