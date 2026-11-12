# deanalvarez.github.io

Personal site, built with Jekyll and deployed by GitHub Pages on push to `master`.
No theme: the design is `_layouts/`, `_includes/` and `assets/css/style.css`.

## Layout

| Path | What |
| --- | --- |
| `_config.yml` | Name, bio, profile links, nav, publication categories |
| `_pages/` | About (home), Background, Publications, Blog index, 404 |
| `_publications/` | One Markdown file per paper; body is the abstract |
| `_posts/` | Blog posts (the Blog nav link appears once there is one) |
| `_drafts/` | Unpublished posts |
| `markdown_generator/` | Scripts to generate publication files from `pubs.bib` (not published) |

## Publication front matter

```yaml
title: "Paper title"
category: conferences   # key from publication_categories in _config.yml
date: 2024-12-15
authors: 'Dean E. Alvarez, Coauthor Name'   # your name is bolded
venue: 'Venue name'
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
docker run --rm -it -p 4000:4000 -v "$PWD":/srv/jekyll -w /srv/jekyll \
  ruby:3.3 sh -c "bundle install && bundle exec jekyll serve -H 0.0.0.0 --livereload"
```
