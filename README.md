# Alia Abdul Aziz — Portfolio

Source for [aliaaziz.work](https://aliaaziz.work), Alia's personal data analyst portfolio.

## Repository layout

```text
CNAME                             Custom domain for GitHub Pages
README.md                         Project and maintenance guide
index.html                        Homepage, styles, scripts, and SVG illustrations
images/
  Singapore-Public-Housing.jpg     Housing project card
  social-preview.png              Link-sharing image
  tableau.png                     Tableau project card
  tiktok.jpeg                     TikTok project card
```

## Features

- Responsive introduction and project cards, with a sticky directory and contact icons.
- Projects section and expandable Other projects collection.
- Research contributions and links to three co-authored publications.
- Singapore weather window with animated skies, sheer curtains, and four selectable cats: Salmah, Tommy, Happy, and Hassan.
- Rose interface accents, a letter-by-letter introduction, and brief link-hover sparkles.
- Search/social metadata and a static sharing image.

Project analysis files and datasets live in their linked repositories, not here.

## Preview

No build step or package installation is required. Open index.html in a browser, or run a static server from this directory:

```sh
python3 -m http.server 8000
```

Then visit http://localhost:8000. Serving locally also makes the name link's root navigation work. Weather requests require internet access and may be restricted in some local-file/browser contexts.

## Weather and preferences

The window requests the [NEA two-hour area forecast via data.gov.sg](https://data.gov.sg/datasets/d_3f9e064e25005b0e42969944ccaf2e7a/view) when the page loads and every 30 minutes. Times use Asia/Singapore. It displays a forecast, not live observed conditions; failed or expired data is labelled accordingly.

The selected cat is stored locally under portfolio-cat when browser storage is available. No geolocation or API key is used. Motion effects respect the visitor's reduced-motion setting.

## Maintaining the site

- Edit index.html for content, styles, interactive behaviour, and the window illustration.
- Keep project image references and files in sync.
- Keep the title, meta description, Open Graph, and Twitter metadata consistent.
- Update images/social-preview.png when the sharing design changes.
- Preserve CNAME unless intentionally changing the domain.
- Preview desktop/mobile layouts, section navigation, Other projects, cat switching, reduced motion, and weather loading/error states before merging changes.

## Deployment and history

The site uses GitHub Pages with the custom domain recorded in CNAME. Publishing follows the repository's configured Pages source; a feature branch is not a live preview.

The original site used the Massively template by [HTML5 UP](https://html5up.net/massively). The current homepage does not load its styles, scripts, or fonts. Unused template/demo files and unreferenced images were removed in the cleanup PR; they remain recoverable through Git history. This repository does not declare a new blanket licence for third-party imagery.
