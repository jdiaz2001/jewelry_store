# Project Structure

```
├── _config.yml          # Jekyll site config (title, base URL)
├── _data/
│   └── catalog.yml      # Product catalog data (ref_code, description, price)
├── _includes/
│   └── products.html    # Product grid partial (Liquid + Tailwind)
├── _layouts/
│   └── default.html     # Base HTML layout (loads Tailwind CDN)
├── images/
│   └── E0001.jpg …      # Product images, named by ref_code
├── index.html           # Home page, includes products.html
├── Gemfile              # Ruby/Jekyll dependencies
└── _site/               # Generated output (do not edit)
```

## Conventions

- Product images are stored in `images/` and named `{ref_code}.jpg` (e.g. `E0001.jpg`).
- Catalog entries live in `_data/catalog.yml` as a flat list of objects with keys: `ref_code`, `description`, `price`.
- Reusable HTML fragments go in `_includes/`. Page-level wrappers go in `_layouts/`.
- `_site/` is the build output — never edit files there directly.
