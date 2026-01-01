PR Summary — Additive UX: mobile categories, smoke tests, docs

What changed:
- Grouped mobile category links under a new "Categories" header in the mobile nav.
- Added small, additive UX features earlier: product modal, mini-cart, desktop categories dropdown, trust badges, and JSON-LD.
- Created a short README describing the edits and how to test locally.

Why:
- Improve navigation on mobile by surfacing categories and allowing quick filtering without navigating away from the gallery.
- Add lightweight product detail and mini-cart experiences to improve conversions while preserving existing WhatsApp ordering flow.

Testing notes:
- Manual smoke checks performed: existence of `filterGalleryByCategory`, `showProductModal`, and `miniCart` elements; mobile links call the filter function.
- No existing UI/logic was removed or refactored; all changes are additive.

Commit message used: "Additive UX: mobile categories, smoke tests, docs"
