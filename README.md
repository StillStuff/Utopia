# Utopia

A concept for a mobile app that pays you, in game currency, for recycling.

Two games — a life simulation and a city management sim, both framed as research
projects run by scientists with questionable judgement — with a recycling system
built into their mechanics. Affiliated brands lay a scannable code into their
packaging; players recycle the item, scan the code, and earn currency they spend
on avatar cosmetics or on real coupons from those brands. A rotating quest system
and permanent achievements sit on top.

The aim is to give teenagers and young adults a tangible reason to recycle.

## Status

Design concept. The marketing site in this repo and the
[Figma prototype](https://www.figma.com/file/jOb9wAshvpnRQLaUK1SSvT/Utopia?node-id=2%3A4)
are what exist — neither game is built, and there are no commercial partners.

## The site

Static HTML with Bootstrap 5.1.3 from a CDN. No build step and no dependencies —
open `index.html` in a browser, or serve the folder:

```sh
python -m http.server 8000
```

| Page | File |
| --- | --- |
| Landing | `index.html` |
| Home (game select) | `Home.html` |
| Media (prototype, screens, brand assets) | `Media.html` |
| About | `About.html` |
| Affiliated Brands | `Brands.html` |
| Community | `Community.html` |
| FAQ | `FAQ.html` |

### Styles

`base.css` holds everything shared — palette, fonts, background, the `.hero`
block. Each page then loads one override file after it: `style.css` (landing),
`hstyle.css` (home), `astyle.css` (about), or `page.css` (shared by Media,
Brands, Community and FAQ).

### Deploying

Settings → Pages → deploy from the `main` branch, root folder. `index.html` is
the entry point.

## Before publishing

- Export the Figma frames into `media/` and swap out the placeholder tiles on
  `Media.html` and `Community.html`.
- Replace the contact address on `Brands.html`.
- The Figma embed on `Media.html` only renders if the file's sharing is set to
  "anyone with the link".
