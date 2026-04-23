# Project Structure

```
├── _config.yml          # Jekyll site config (title, description, base URL)
├── _data/
│   └── catalog.yml      # Product catalog data (ref_code, description, price, category)
├── _includes/
│   └── products.html    # Product grid with sidebar filters, search, sort, and JS logic
├── _layouts/
│   └── default.html     # Base HTML layout (header, footer, Tailwind CDN, i18n script)
├── images/
│   └── E0001.jpg …      # Product images, named by ref_code
├── index.html           # Home page (hero banner + products include)
├── Gemfile              # Ruby/Jekyll dependencies
└── _site/               # Generated output (do not edit)
```

## Conventions

- Product images are stored in `images/` and named `{ref_code}.jpg` (e.g. `E0001.jpg`).
- Catalog entries live in `_data/catalog.yml` as a flat list of objects with keys: `ref_code`, `description`, `price`, `category`.
- Valid categories: `aretes`, `dijes`, `anillos`.
- Reusable HTML fragments go in `_includes/`. Page-level wrappers go in `_layouts/`.
- `_site/` is the build output — never edit files there directly.
- All translatable UI text uses `data-i18n` attributes. Translations are defined in the i18n script block in `default.html`.
- The hero banner lives in `index.html`, not in an include.
