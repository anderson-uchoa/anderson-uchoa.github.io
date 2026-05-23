# anderson-uchoa.github.io

Personal academic website of **Anderson Uchôa** — Software Engineering researcher at UFC & NC State.

Built with [Jekyll](https://jekyllrb.com/) and hosted on [GitHub Pages](https://pages.github.com/).

## Structure

```
.
├── _config.yml          # Jekyll configuration
├── _layouts/            # Page layouts (default.html)
├── _includes/           # Reusable partials (nav, footer, head, scripts)
├── _data/
│   ├── i18n/
│   │   ├── en.yml       # English UI strings
│   │   └── pt-BR.yml    # Portuguese UI strings
│   ├── profile.yml      # Academic positions and education
│   ├── news.yml         # Recent news items
│   ├── awards.yml       # Best papers, grants, and volunteer awards
│   ├── research.yml     # Research projects (ongoing and completed)
│   ├── teaching.yml     # Courses taught per institution
│   └── services.yml     # Conference PC memberships and journal reviews
├── publications/
│   └── UchoaPapers.bib  # BibTeX file (publication count auto-detected)
├── pt-BR/               # Portuguese versions of all pages
├── css/ / js/ / img/    # Static assets
└── .github/workflows/
    └── deploy.yml       # Build and deploy to GitHub Pages via Actions
```

## Multilingual support

The site supports **English** (default) and **Portuguese (PT-BR)**. Pages under `pt-BR/` set `lang: pt-BR` in their front matter; all templates and layouts read `_data/i18n/<lang>.yml` for UI labels. Content data (`_data/*.yml`) is shared between both languages — adding a new entry to any data file automatically reflects in both versions.

## Adding content

| What | Where |
|------|-------|
| New publication | Add entry to `publications/UchoaPapers.bib` |
| News item | Add entry to `_data/news.yml` |
| Award or grant | Add entry to `_data/awards.yml` |
| Research project | Add entry to `_data/research.yml` |
| Course | Add entry to `_data/teaching.yml` |
| Conference/journal service | Add entry to `_data/services.yml` |

## Local development

Requires [Bundler](https://bundler.io/) and the Homebrew (or system) Ruby with write access.

```bash
bundle install
bundle exec jekyll serve
```

The site is then available at `http://localhost:4000`.

## Deployment

Pushing to `master` triggers the GitHub Actions workflow (`.github/workflows/deploy.yml`), which builds the site with `bundle exec jekyll build` and deploys it to GitHub Pages automatically.

## License

MIT — see [LICENSE](LICENSE).
