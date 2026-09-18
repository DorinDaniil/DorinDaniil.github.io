# dorindaniil.github.io

Personal academic website of Daniil Dorin, built with [Hugo](https://gohugo.io) and custom templates (no external theme).

## Structure

```
hugo.yaml                 site config, author info, social links, menu
content/
  _index.md               about text on the home page
  research/<slug>/        one page bundle per paper: index.md + figures
  projects/<slug>/        one page bundle per open-source project
  publications.md         renders data/publications.yaml
  talks.md                renders data/talks.yaml and data/posters.yaml
data/
  publications.yaml       full publication list (journal, DOI, code links)
  talks.yaml, posters.yaml
  teaching.yaml, awards.yaml
layouts/                  templates: baseof, home, section, page, partials
assets/css/main.css       styles (processed and fingerprinted by Hugo Pipes)
static/                   avatar, favicon
.github/workflows/hugo.yml  builds and deploys to GitHub Pages on push to main
```

## Adding content

- **New paper:** create `content/research/<slug>/index.md` with front matter (`title`, `authors`, `venue`, `year`, `links`, `cover`, `summary`) and drop figures next to it. Reference them as `![caption](figure.png)`.
- **New project:** same in `content/projects/<slug>/`.
- **Publication list:** append an entry to `data/publications.yaml`.

## Local preview

```bash
hugo server -D
```

## Deploy

Push to `main`. In the repository settings set **Pages → Source → GitHub Actions**. The workflow builds the site and publishes it to https://dorindaniil.github.io.
