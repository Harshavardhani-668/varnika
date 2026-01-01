Title: Additive UX — Product modal, mini-cart, categories (mobile & desktop)

Summary
-------
This PR introduces a set of small, additive UX improvements designed to increase clarity and conversions while preserving the exact current UI, layout, and functionality.

What changed (additive only)
- Hero: added a one-line value proposition and an extra CTA button “Explore Handmade Gifts” that smoothly scrolls to the gallery.
- Desktop: added a `Categories` dropdown that filters the gallery client-side.
- Mobile: added grouped category links under a small **Categories** header in the mobile menu (client-side filtering). These new links do not remove or change existing mobile menu items.
- Product detail: lightweight client-side modal (no back-end) showing image, title, static price, specs, and both **Order Now via WhatsApp** and **Add to Cart** buttons. Uses existing `addToCart` where available.
- Mini-cart: floating additive mini-cart panel reading `localStorage` (`varnika_cart`), allowing quantity updates (calls existing functions), remove, and a “Proceed to WhatsApp Checkout” action that builds the order message.
- Trust badges: small "Handmade" / "Customizable" badges inserted into gallery cards.
- SEO: added lightweight client-side JSON-LD generated from gallery items (non-blocking).
- Reviews: left your on-site review system unchanged (still auto-published); removed the WhatsApp review sender earlier and replaced with on-site localStorage reviews in previous edits.

Crucial notes (do NOT change)
- WhatsApp ordering links for products remain exactly as before; every product-order WhatsApp button still opens WhatsApp with order details.
- Cart logic (`addToCart`, `updateQuantity`, `removeFromCart`, WhatsApp checkout) is left intact and is reused by the new mini-cart.
- No existing UI, animations, or layout were removed or refactored — all changes are additive and safe.
- No admin review UI or testimonial workflow changes were added.

Screenshots
----------
- `pr-assets/screenshot-hero.svg` — hero area + CTA (placeholder screenshot)
- `pr-assets/screenshot-mobile-categories.svg` — mobile menu Categories (placeholder screenshot)

Testing notes
-------------
- Verify desktop Categories dropdown filters gallery items.
- Verify mobile menu > Categories filters gallery and scrolls to section.
- Click a product image/title to open modal; test "Order Now via WhatsApp" and "Add to Cart".
- Open the mini-cart, test qty +/- and Remove; click "Proceed to WhatsApp Checkout" and confirm the message.

Commit: Additive UX: mobile categories, smoke tests, docs
