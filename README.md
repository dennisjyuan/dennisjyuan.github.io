# dennisjyuan.github.io

Personal academic homepage. Jekyll, built automatically by GitHub Pages on every
push to `master`. Based on the [Minimal Light](https://github.com/yaoyao-liu/minimal-light)
theme, extended with a research-theme grouping.

## Where to edit things

You almost never need to touch HTML. Content lives in three YAML files:

| I want to...                        | Edit                                        |
| ----------------------------------- | ------------------------------------------- |
| Add a paper                         | `_data/publications.yml`                    |
| Add/rename a research theme         | `_data/themes.yml`                          |
| Add a news item                     | `_data/news.yml`                            |
| Change the About text               | `index.md`                                  |
| Change name, title, email, links    | `_config.yml`                               |
| Change appointments/education/awards| `_includes/background.md`                   |
| Change talks                        | `_includes/talks.md`                        |
| Change spacing, colors, type        | `assets/css/custom.css`                     |

### Adding a publication

Copy an existing block at the top of `_data/publications.yml`. The `theme:` field
decides which research theme it appears under; it must match an `id:` in
`_data/themes.yml`. Use `theme: other` to keep a paper out of the Research
section while still listing it under Publications. Wrap your own name in
`<strong>` tags. Set `highlight: true` to give it a "featured" badge.

Order in the file is the order on the page, so put new papers first.

### Careful with YAML

Indentation is significant and a stray tab or unquoted colon will fail the build.
If the site stops updating after a push, check the Actions tab on GitHub for the
build error.

## Previewing locally (optional)

```
bundle install
bundle exec jekyll serve
```

Then open http://localhost:4000.
