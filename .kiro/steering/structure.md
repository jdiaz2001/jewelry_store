# Project Structure

```
├── _config.yml          # Jekyll site config (title, description, base URL)
├── _data/
│   ├── aretes.yml       # Aretes (earrings) catalog
│   ├── anillos.yml      # Anillos (rings) catalog
│   ├── arracadas.yml    # Arracadas (hoop earrings) catalog
│   ├── bolsas.yml       # Bolsas (bags) catalog
│   ├── collares.yml     # Collares (necklaces) catalog
│   ├── dijes.yml        # Dijes (pendants) catalog
│   └── ear_cuff.yml     # Ear cuff catalog
├── _includes/
│   └── products.html    # Product grid with sidebar filters, search, sort, and JS logic
├── _layouts/
│   └── default.html     # Base HTML layout (header, footer, Tailwind CDN, i18n script)
├── images/
│   └── {category}/{ref_code}.jpg  # Product images organized by category folder
├── index.html           # Home page (hero banner + products include)
├── Gemfile              # Ruby/Jekyll dependencies
└── _site/               # Generated output (do not edit)
```

## Conventions

- Product images are stored in `images/{category}/` and named `{ref_code}.jpg` (e.g. `images/aretes/E0001.jpg`).
- Each category has its own data file in `_data/`. Entries are a flat list of objects with keys: `ref_code`, `description`, `price`. The category is inferred from the file name.
- Valid categories (file names): `aretes`, `anillos`, `arracadas`, `bolsas`, `collares`, `dijes`, `ear_cuff`.
- To add a new category, create `_data/{category}.yml` and add the category name to the `categories` array in `_includes/products.html`.
- Reusable HTML fragments go in `_includes/`. Page-level wrappers go in `_layouts/`.
- `_site/` is the build output — never edit files there directly.
- All translatable UI text uses `data-i18n` attributes. Translations are defined in the i18n script block in `default.html`.
- The hero banner lives in `index.html`, not in an include.
