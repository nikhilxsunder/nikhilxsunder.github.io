<div align="center">

# nikhilxsunder.github.io

**Personal website of Nikhil Sunder** — quantitative economics, research software, and open-source infrastructure for computational economics.

[![Live site](https://img.shields.io/badge/live-nikhilxsunder.github.io-blue.svg)](https://nikhilxsunder.github.io)
[![Built with Jekyll](https://img.shields.io/badge/built%20with-Jekyll-CC0000.svg?logo=jekyll&logoColor=white)](https://jekyllrb.com/)
[![Deploy](https://github.com/nikhilxsunder/nikhilxsunder.github.io/actions/workflows/pages.yml/badge.svg)](https://github.com/nikhilxsunder/nikhilxsunder.github.io/actions)

</div>

---

## Overview

A static Jekyll site built on the [minima](https://github.com/jekyll/minima) theme, deployed via GitHub Pages. It serves as the public index for my research, open-source packages, and affiliations.

| Page | Path | Contents |
|---|---|---|
| Home | `/` | Landing page and stack overview |
| About | `/about/` | Background, research interests, contact |
| Development | `/development/` | Package portfolio — `fedfred`, `edgar-sec`, `toros`, `cultivars`, `ns-sdn`, `autofed` |
| Research | `/research/` | Publications and citable software artifacts |
| Groups | `/groups/` | ICSRI and toros-dev affiliations |
| Press | `/press/` | External coverage |

## Local development

Requires Ruby 3.x and Bundler.

```shell
git clone https://github.com/nikhilxsunder/nikhilxsunder.github.io.git
cd nikhilxsunder.github.io
bundle install
bundle exec jekyll serve --livereload
```

The site builds to `_site/` and serves at `http://localhost:4000`.

To update dependencies:

```shell
bundle update
bundle exec jekyll serve   # verify before committing Gemfile.lock
```

## Structure

```text
.
├── _config.yml        # Site configuration, nav order, plugins
├── index.md           # Landing page
├── about.md
├── development.md
├── research.md
├── groups.md
├── press.md
├── assets/            # Images, banners, favicon
└── Gemfile            # Jekyll and plugin dependencies
```

## Plugins

| Plugin | Purpose |
|---|---|
| `jekyll-feed` | Atom feed generation |
| `jekyll-seo-tag` | Meta tags, Open Graph, JSON-LD structured data |
| `jekyll-sitemap` | `sitemap.xml` for search indexing |
| `jekyll-redirect-from` | Permalink redirects for renamed pages |

## Deployment

Pushes to `main` deploy automatically through GitHub Pages. No manual build step.

## Related

- [`fedfred`](https://github.com/nikhilxsunder/fedfred) — Federal Reserve FRED/ALFRED/GeoFRED/FRASER client
- [`edgar-sec`](https://github.com/toros-dev/edgar-sec) — SEC EDGAR REST API client
- [`toros`](https://github.com/toros-dev/toros) — DataFrame extension for financial objects
- [`cultivars`](https://github.com/nikhilxsunder/cultivars) — Bayesian and structural VAR modeling
- [`ns-sdn`](https://github.com/nikhilxsunder/ns-sdn) — Neural spectral state-space architecture

## License

Site content © 2026 Nikhil Sunder. Source code available under the [MIT License](LICENSE).
