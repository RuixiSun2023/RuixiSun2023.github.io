# Ruixi Sun

Personal research website: https://ruixisun2023.github.io/

Built with Jekyll and al-folio. Push changes to `main` to publish through GitHub Actions. Repository Settings → Pages must use **GitHub Actions** as its source.

## Editing

- Introduction and research interests: `_pages/about.md`
- Publications and PDF links: `_bibliography/papers.bib`
- Full-text papers: `assets/pdf/` (11 papers)
- Experience: `_data/experience.yml`; education: `_data/cv.yml`
- Photo journal: `_data/gallery.yml` and `assets/img/gallery/`
- Google Scholar: `_data/socials.yml`
- Shared styling: `assets/css/site-editorial.css`

## Local preview

Install Ruby 3.3, Bundler, Node.js and ImageMagick, then run:

```sh
bundle install
bundle exec jekyll serve --host 127.0.0.1
```

Visit http://127.0.0.1:4000/. The production site lives at the domain root, so `baseurl` is empty. Local theme overrides are acknowledged in `.al-folio-overrides.yml`.

The theme's MIT license is preserved in `LICENSE`. Personal photographs and paper PDFs are not relicensed by the theme license; their respective rights remain with their owners.
