# Tech Stack

- **Static site generator**: Jekyll 4.3+
- **Language**: Ruby (build tooling only), HTML, Liquid templates, vanilla JavaScript
- **CSS**: Tailwind CSS via CDN (`https://cdn.tailwindcss.com`)
- **Data format**: YAML for catalog data
- **Package manager**: Bundler (Gemfile)

## Common Commands

```bash
# Install dependencies
bundle install

# Serve locally with live reload
bundle exec jekyll serve

# Build for production
bundle exec jekyll build
```

## Notes

- No JavaScript framework — pure static HTML + Tailwind utility classes + vanilla JS for interactivity.
- Tailwind is loaded from CDN, not compiled locally. No `tailwind.config.js` or build step for CSS.
- The site defaults to Spanish (`<html lang="es">`) with a client-side English toggle. Language preference is stored in `localStorage`.
- All UI text translation is handled via `data-i18n` attributes and a JS translation dictionary in `default.html`.
- Product data (names, descriptions) stays in Spanish regardless of language toggle.
- Color palette uses Tailwind's `rose` for primary accent and `emerald` for the WhatsApp contact button.
- SEO: Open Graph and Twitter Card meta tags are in `default.html` `<head>`.
