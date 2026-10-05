# Tirupati Food Plaza - Website Source Code

Plain HTML, CSS and JavaScript. No build step, no framework, no dependencies
(only Google Fonts: Fraunces and Outfit, loaded from the internet).

## Files
- `index.html`   Page structure (header, hero slideshow, huts, menu page, contact, footer, popup)
- `style.css`    All styling. Colours are CSS variables at the top (`:root`)
- `script.js`    Menu data, slideshow, menu page routing, popup, WhatsApp form, open/closed badge
- `images/`      Logos for the 7 huts and the bakery (transparent WebP), hero slideshow photos, popup poster

## How to run
Open `index.html` in a browser, or upload the whole folder to any web host
(cPanel public_html, Netlify, Vercel, GitHub Pages, etc.).

## Common edits
- **Menu items and prices:** `script.js`, array `H`, field `m`.
  Format `"Item name:price"` separated by `;`. Add `:n` at the end for non-veg.
  Example: `'Hyderabadi Veg Biryani:229;Steam Rice:99'`. Add `:s` at the end for a house special (shows a star), `:n` for non-veg.
- **Add or rename a hut:** `script.js`, array `H` (id, name, logo, ac = accent colour, tag, cu, m).
  Put its logo in `images/` and point `logo` to it.
- **Phone, address, timings:** search for `95271 10254`, `919527110254`, `Washim` and `11:00 AM`
  in `index.html` and `script.js` (also the JSON-LD block in `<head>` and the open/closed
  badge function `stat()` in `script.js`).
- **Hero slideshow photos:** replace `images/slide-1.jpg` to `slide-5.jpg`, or edit the `.sl` divs
  in `index.html`. Captions are in the `CAP` array in `script.js`.
- **Popup poster:** replace `images/popup.jpg`. To remove it, delete the `<div class="pop" ...>` block.
- **Colours:** `:root` in `style.css` (ivory, coffee, caramel, gold).
- **Developer credit:** footer in `index.html`.

## Notes
- The menu is a separate "page" handled by the URL hash (`#/menu`, `#/menu/dhaba`).
- The contact form sends the enquiry through WhatsApp (`wa.me`). Replace it with a
  server form or email service if you want enquiries delivered by email.
- The menu prices are sample values until the final menu is supplied.
- For WordPress + Elementor: rebuild the sections with the same colours and fonts, or have
  the developer convert this into a theme.

- **Gallery:** `script.js`, array `G` (image, caption, hut, category: plaza / food / drinks). Add photos to `images/` and add a line.
