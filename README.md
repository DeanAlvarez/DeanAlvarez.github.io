# deanalvarez.github.io

Personal site, built with Jekyll and deployed by GitHub Pages on push to `master`.
No theme: the design is `_layouts/`, `_includes/` and `assets/css/style.css`.

## Layout

| Path | What |
| --- | --- |
| `_config.yml` | Name, bio, profile links, nav, publication categories |
| `_pages/` | About (home), Background, Publications, Blog index, 404 |
| `_data/cv.yml` | Background page content (mirrors the LaTeX CV) |
| `_publications/` | One Markdown file per paper; body is the abstract |
| `_posts/` | Blog posts (the Blog nav link appears once there is one) |
| `_drafts/` | Unpublished posts |
| `markdown_generator/` | Old template scripts for generating publication files (not published) |

## Publication front matter

```yaml
title: "Paper title"
category: conference    # conference | preprint | report (publication_categories in _config.yml)
tags: ["Demo"]          # optional badges
selected: true          # optional; listed under Selected Publications on the home page
date: 2024-12-15        # used for sorting, and shown if the venue has no year
authors: 'Dean E. Alvarez, Coauthor Name'   # your name is bolded
venue: 'SIGIR 2025'
paperurl: https://...
codeurl: https://...    # optional
slidesurl: https://...  # optional
citation: '...'
```

## Posts with math or visualizations

Add `math: true` to load MathJax, and `scripts:` (a list of URLs or `/assets/js/...` paths)
to load JavaScript at the end of the page. Wrap a figure in `<figure class="wide">` to let it
extend past the text column. See `_drafts/research-overview.md`.

## Running locally

```bash
bundle install
bundle exec jekyll serve --livereload   # add --drafts to include _drafts/
```

Or without Ruby installed:

```bash
docker run --rm -it -p 4000:4000 -u "$(id -u):$(id -g)" -e HOME=/tmp -e BUNDLE_PATH=vendor/bundle \
  -v "$PWD":/srv/jekyll -w /srv/jekyll \
  ruby:3.3 sh -c "bundle install && bundle exec jekyll serve -H 0.0.0.0 --livereload"
```

`jekyll serve` doesn't reload `_config.yml`; restart it after editing that file.
