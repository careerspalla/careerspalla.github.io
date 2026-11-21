# DayCatch Fish & Chips — Website

## What changed
- **Design**: rebuilt around a 3-colour palette — Ink Navy `#0B2340`, Shell Ivory `#F6F2EA`, and Brass `#B08A4E` — with generous whitespace and a clear type hierarchy. Removed the neon glow text, red lettering, busy gradients and per-tier rainbow colours.
- **Typography**: Fraunces (serif, headings) + Inter (sans, body/UI), loaded from Google Fonts.
- **CSS**: moved out of the inline `<style>` block into `css/style.css`, so future edits are easy and the file loads faster (browsers cache it separately).
- **Background art**: `images/brand/wave-pattern.svg`, `wave-divider.svg` and `favicon.svg` are original vector artwork made for this site — royalty-free and unique to DayCatch, no stock-photo licensing to worry about.
- **Images**: product photos were resized/compressed for the web (from ~17 MB to ~1.6 MB total) so pages load quickly, especially on mobile data.
- **Mobile**: layout, type sizes, spacing and the hero image all adapt down to small phone screens (see `css/style.css`, the "Mobile refinements" section at the bottom).
- **SEO**: descriptive title/meta description, Open Graph + Twitter cards, a JSON-LD structured-data block (`Organization` + one `FastFoodRestaurant` entry per outlet, so Google can understand your locations and hours), a `robots.txt` and `sitemap.xml`, corrected/descriptive `alt` text on every image, and semantic heading order.

## File structure
```
├── index.html
├── css/
│   └── style.css
├── images/
│   ├── brand/          (favicon + original SVG artwork)
│   └── fishchips/       (your product photos, optimised)
├── robots.txt
└── sitemap.xml
```

## Run it locally
No build step needed — it's a static site.
1. Unzip the folder.
2. Open `index.html` directly in a browser, **or** for the most accurate preview, serve it locally:
   ```
   cd dcfcwebsite
   python3 -m http.server 8000
   ```
   then visit `http://localhost:8000`.

## Publish it
Upload the entire contents of this folder (keeping the same structure) to your web host's root directory, so that `index.html`, `css/`, `images/`, `robots.txt` and `sitemap.xml` all sit alongside each other.

## Before you go live — a few things to double-check
- **Domain**: the SEO tags assume `https://www.fishandchips.in/`. If that's not the final domain, search-and-replace it in `index.html`, `robots.txt` and `sitemap.xml`.
- **Social links**: the Facebook/Instagram/LinkedIn icons in the footer currently point to `#` — add your real profile URLs when ready.
- **Google Search Console**: once live, submit `sitemap.xml` there to help Google index the site faster.
- **Google Business Profiles**: for the best "near me" search results, make sure each of your 4 outlets also has its own Google Business Profile — this pairs well with the structured data already on the page.
