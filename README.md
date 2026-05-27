# AP Guppy World — Website

A complete rebuild of the AP Guppy World site: a single-page, mobile-first
store for guppies, bettas, aquarium care and live plants, with a cart that
sends orders straight to WhatsApp.

## What's in this folder

    index.html        →  the entire website (HTML + CSS + JavaScript in one file)
    images/
      brand/          →  logo + favicon
      products/       →  fish & product cut-outs (transparent)
      trending/       →  trending variety photos
      gallery/        →  gallery photos
      hero.jpg, about-*.jpg

There is no build step and no server code. It is a static site.

## How to put it online (GitHub Pages)

1. Copy `index.html` and the `images/` folder into your GitHub Pages repo
   (replacing the old files).
2. Commit and push.
3. Your site updates automatically at your GitHub Pages address.

It also works by simply double-clicking `index.html` to preview locally.
(The Google Map only loads on a real web address, not from a local file —
that is normal.)

## ★ How to add a PHOTO or VIDEO to a guppy variety

Open `index.html` and find the `PRODUCTS` list inside the `<script>` near the
bottom. Each variety is one line, for example:

    {id:"g-hb-silverado", cat:"guppy", name:"HB Silverado",
     desc:"Half-black silver shimmer", price:150, unit:"pair",
     img:"", video:""},

To add media, fill in `img` and/or `video`:

  • Photo  →  put your picture in `images/products/` and set the path:
              img:"images/products/hb-silverado.png"

  • Video  →  paste a YouTube link:
              video:"https://youtu.be/XXXXXXXXXXX"
              (normal links and Shorts links both work)

Leave them as `""` to keep the "Photo & video coming soon" placeholder.
A variety with a video shows a play button; tapping a card opens the
photo/video in a pop-up.

## How the cart works

Customers add items, open the cart, and tap **Send Order on WhatsApp**.
This opens WhatsApp with the full order (items, quantities, total) pre-typed,
addressed to +91 89405 24235. You then confirm stock, packing and shipping.

To change the WhatsApp number, edit the `WA` value at the top of the script.

## Updating prices, products or text

Everything is in the `PRODUCTS`, `TRENDING`, `TESTIMONIALS` and `GALLERY`
lists in the script — edit a value, save, and re-upload `index.html`.
