# Amma Restaurant — Website

A single-page marketing website for **Amma Restaurant**, Sathuvachari, Vellore — South Indian, Chettinad, Tandoor and Biryani. Built as one self-contained `index.html` file: no build tools, no framework, no dependencies to install.

## What's in this project

- `index.html` — the entire website (structure, styling, and behaviour all in one file)
- Your food photos (`01-hero-biryani.jpg`, `02-pick-mutton-biryani.webp`, etc.) — sit alongside `index.html`, not in a subfolder
- `amma-restaurant-menu.pdf` *(optional, not included)* — add this yourself if you want the "Download / Print Menu" button to work

## Folder setup

```
Amma Restaurant/
├── index.html
├── amma-restaurant-menu.pdf      ← optional, add if you have it
├── 01-hero-biryani.jpg
├── 02-pick-mutton-biryani.webp
├── 03-pick-mutton-chukka.webp
├── 04-pick-tandoori-chicken.webp
├── 05-pick-butter-chicken.webp
├── 06-pick-ghee-roast-dosa.webp
├── 07-pick-royal-falooda.webp
├── 08-chef-special-biryani.webp
├── 09-event-hosting.webp
├── 10-dine-in.webp
├── 11-cat-starters.webp
├── 12-cat-soup.webp
├── 13-cat-rice.webp
├── 14-cat-tandoor-kebab.webp
├── 15-cat-biryani.webp
├── 16-cat-gravies.webp
├── 17-cat-dosa.webp
├── 18-cat-desserts.webp
├── 19-review-rating-biryani.webp
├── 20-review-cta-tandoori.webp
├── 21-strip-biryani.webp
├── 22-strip-tandoori.webp
├── 23-strip-event.webp
├── 24-strip-falooda.webp
└── 25-strip-dosa.webp
```

Everything is flat — no `images/` subfolder. `index.html` already points straight at these filenames.

## Viewing it

Double-click `index.html` to open it in any browser. No server, no npm install, nothing to build.

## What's on the page

- **Sticky nav** with a mobile hamburger menu
- **Hero banner** with restaurant name and call-to-action
- **Favourites carousel** — swipeable cards for standout dishes (Mutton Biryani, Tandoori Chicken, Butter Chicken, etc.)
- **Chef's special** and **event hosting / dine-in** feature cards
- **Category strip** — eight round icons linking down to matching sections of the full menu
- **Full menu** — paged by category, with a downloadable/printable PDF button
- **Reviews** — a rotating carousel of real Google reviews, plus a Zomato rating card and a "Write a Google Review" call-to-action
- **Photo strip**
- **Find Us / Amenities panel** with contact details and hours
- **FAQ accordion**
- **Live open/closed status** — calculated from the restaurant's hours (7:00–16:00 & 18:30–22:30 IST) using the visitor's local time, updated every minute
- **Back-to-top button**, smooth scrolling, scroll-reveal animations

## Tech notes

- Pure HTML/CSS/vanilla JS — everything lives in `index.html`
- Fonts: Fraunces (headings) and Karla (body), loaded from Google Fonts — needs an internet connection to show correctly
- Images use CSS `object-fit: cover` throughout, so photos crop to fill their frame cleanly regardless of original size or aspect ratio
- `loading="lazy"` is set on every image for faster initial page loads
- Responsive breakpoints handle tablet (900px) and mobile (680px) layouts

## Customizing content

| To change... | Edit... |
|---|---|
| Phone number, address, hours | Search for the contact/hours section near "Find Us" |
| Dish names/descriptions in Favourites | The `.pick-card` blocks |
| Menu items | The menu data feeding `#menu-track` |
| Reviews | The `REVIEWS` array near the bottom of the `<script>` |
| Colors/fonts | The `:root` CSS variables at the top (`--gold`, `--ink`, `--rust`, etc.) |
| Which photo goes where | Swap the `src="..."` on the relevant `<img>` tag — see the image map below |

### Image map

| File | Used for |
|---|---|
| `01-hero-biryani.jpg` | Hero banner + social share preview |
| `02–07-pick-*.webp` | Favourites swipeable dish cards |
| `08-chef-special-biryani.webp` | Chef's special feature |
| `09-event-hosting.webp` | Event hosting card |
| `10-dine-in.webp` | Dine-in card |
| `11–18-cat-*.webp` | Category circles (Starters, Soup, Rice, Tandoor, Biryani, Gravies, Dosa, Desserts) |
| `19-review-rating-biryani.webp` | Zomato rating card |
| `20-review-cta-tandoori.webp` | "Write a Google Review" card |
| `21–25-strip-*.webp` | Photo strip above the contact/reservation section |

If you rename or swap any image, either match the new filename to the existing `src=`/`content=` attribute, or update that attribute in `index.html` to point at the new name.

## Publishing it online

This is a static site, so any static host works. A few easy free options:
- **Netlify** or **Vercel** — drag-and-drop the whole folder in their web dashboard
- **GitHub Pages** — push the folder to a GitHub repo and enable Pages in settings
- Any regular web hosting (cPanel, etc.) — upload the folder via FTP

Whichever you choose, upload the **whole folder together** (HTML + all image files) so the paths keep working.
