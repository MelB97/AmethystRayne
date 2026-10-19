# Amethyst Rayne Eclectic Creations — catalogue site

Static site (no build step) for Netlify. Everything on the page comes from `data/catalogue.json`.

## Adding new pieces (photo dumps)
**Easiest — Pages CMS (app.pagescms.org):** open this repo → Catalogue → Products → Add an entry.
Pick the shelf, type the name and price, upload one or more photos (the first is the cover), tick *New* if you want the badge. Save — Netlify republishes in about a minute.

**Manually:** drop photos in `images/products/` and add an entry to `items` in `data/catalogue.json`:
```json
{"name":"Bat Wing Shawl","category":"wearables","price":"$45","photos":["images/products/bat-wing-shawl.jpg"],"description":"","availability":"","new":true,"sold_out":false}
```
Products show in the order they appear in the file, grouped under their shelf.
To add a whole new shelf, add it to `categories` (and to the shelf list in `.pages.yml`).

## Buy now buttons
They open the link in `settings.messenger_link` and copy an order message ("Hi! I'd like to order: …") for the customer to paste.
For Messenger to open straight to a chat, change it to `https://m.me/<your-page-username>`.

Photos: aim for square-ish or portrait photos; cards crop to 4:5. Keep files under ~1MB (900–1200px wide is plenty).
