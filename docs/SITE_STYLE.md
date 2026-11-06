# Personal site visual style

The site follows the Gallery's editorial typography: serif headings, sans-serif body text, full-color uncropped photographs, fine rules, and a restrained red accent.

- `assets/css/site-editorial.css` owns shared fonts, colors, navigation, page headers, content widths, footer, and publication styling. Main headings, navigation, and body edges should align across pages.
- `assets/css/photo-journal.css` owns only photo layouts and captions.
- `assets/css/experience.css` owns only experience rows and section layout.
- `assets/css/home.css` owns the homepage introduction/photo grid, research columns, and selected-publications heading. The homepage keeps the name as its main heading and uses “About me” as the eyebrow.
- Page-specific stylesheets are declared with `stylesheet` in front matter and loaded in the document head.
- Light and dark theme colors are defined centrally. Use `--site-accent`, `--site-muted`, and `--site-rule` rather than separate page palettes.
- The shared container is 1160 px with 40 px desktop / 22 px mobile padding. Reading layouts can vary inside that container.
- `footer_fixed: false` keeps the footer after page content throughout the site.

## Personal-site overrides

Two supported local overrides of `al_folio_core` 1.0.15 are tracked in `.al-folio-overrides.yml`:

- `_layouts/default.liquid`: loads shared/page-specific CSS and identifies the page for scoped styles.
- `_includes/header.liquid`: keeps the Ruixi Sun home link visible on the homepage as well as interior pages.

All remaining layout, navigation behavior, search, image previews, and citation behavior comes from the installed gems. Review the tracked overrides when upgrading the theme.

The upstream starter's `npm run lint:style-contract` forbids any `_layouts` or `_includes` directory. As documented in `docs/ARCHITECTURE.md`, this restriction is for the upstream starter, not a customized personal site; the command reports these two directories here. Its checks have not been disabled. Use the override audit, Jekyll build, formatting check, and browser checks to validate this site customization.
