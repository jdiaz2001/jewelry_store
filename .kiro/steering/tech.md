# Tech Stack

- **Static site generator**: Jekyll 4.3
- **Language**: Ruby (build tooling only), HTML, Liquid templates
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

- No JavaScript framework — pure static HTML + Tailwind utility classes.
- Tailwind is loaded from CDN, not compiled locally. No `tailwind.config.js` or build step for CSS.
- The site language is Spanish (`<html lang="es">`). Keep all user-facing text in Spanish.
