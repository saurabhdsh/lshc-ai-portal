# LSHC AI Engineering Portfolio

Static website, five pages, no build step. It does not depend on any framework.

## Files

| File | Purpose |
|---|---|
| `index.html` | Home: hero, index, offering teasers, the system, contact |
| `harness.html` | Harness Engineering Platform |
| `weave.html` | Weave |
| `qeval.html` | QEVAL (formerly Qubit) |
| `tokenops.html` | TokenOps |
| `style.css` | All styles: colour and font tokens at the top, then components and animation |
| `site.js` | Motion on/off toggle in the footer (remembered per browser) |
| `logo.svg` | TCS logo, cropped |

## Run locally

Open `index.html` in a browser, or serve the folder:

```
python3 -m http.server 8080
```

Then visit http://localhost:8080.

## Deploy

Copy the folder to any static host (an intranet web server, SharePoint site assets, Azure Static Web Apps, S3 and similar). Keep all files in the same folder; pages link to each other with relative paths.

Fonts load from Google Fonts. If your network blocks it, the pages fall back to system fonts; to avoid that, self-host Archivo, Instrument Sans and IBM Plex Mono and update the `<link>` in each page.

## Placeholders to replace

- Contact block in `index.html`: owner name, role, email
- QEVAL scorecard values and release threshold in `qeval.html`
- Spend, budget and share figures in `tokenops.html`
- Story ID in the Harness run diagram in `harness.html`

## Editing

- Colours and fonts: the `:root` block at the top of `style.css`
- The header and footer are repeated in each page; change all five when you edit them
