# bekahoverbey.com

Personal author website for Bekah Overbey — built with Jekyll.

## Quick Start

```bash
# Install dependencies
bundle install

# Serve locally
bundle exec jekyll serve
```

Then visit `http://localhost:4000`.

## Adding Fonts (Self-Hosted — No Google Tracking)

This site uses **no external font requests**. Fonts are self-hosted for full privacy. To set them up:

1. Go to [google-webfonts-helper](https://gwfh.mranftl.com/fonts)
2. Download these fonts as `.woff2`:
   - **Playfair Display** — weights: 400, 400i, 500, 500i
   - **Dancing Script** — weights: 400, 500, 600
   - **Nunito Sans** — weights: 300, 300i, 400, 400i
3. Place the files in `assets/fonts/`
4. The filenames should match what's in `assets/css/fonts.css`

Until the font files are added, the site gracefully falls back to system fonts (Georgia, Segoe UI, etc.) which still look great.

## Adding Book Covers & Author Photo

Drop your images into `assets/images/` and update the `index.html` to swap the placeholder `<div>` elements for `<img>` tags. Each book section has a comment showing the exact replacement — for example:

```html
<!-- Replace with: -->
<img src="/assets/images/hideaway.jpg" alt="Hideaway book cover" class="book-cover">
```

Same for the author photo in the About section:

```html
<img src="/assets/images/bekah-author.jpg" alt="Bekah Overbey" class="about-image">
```

## Deploying

This is a standard Jekyll site. You can deploy to:

- **GitHub Pages** — push to a repo and enable Pages in settings
- **Netlify** — connect the repo and it auto-builds
- **Any static host** — run `bundle exec jekyll build` and upload the `_site/` folder

## Structure

```
├── _config.yml          # Site config
├── _layouts/
│   └── default.html     # Base HTML layout
├── assets/
│   ├── css/
│   │   └── style.css    # All styles
│   └── images/          # Book covers & author photo
├── index.html           # Single-page site content
├── Gemfile              # Ruby dependencies
└── README.md
```

## Customizing

- **Colors**: Edit CSS variables at the top of `assets/css/style.css`
- **Fonts**: Swap the Google Fonts link in `_layouts/default.html`
- **Content**: Edit `index.html` — it's all plain HTML with Liquid templating
- **New books**: Copy a `<article class="book-item">` block and update the details
