# Dinner Chooser

A tiny single-page app that helps you decide what's for dinner. Tap a button and it randomly picks one option from your list. You can add or remove options, and your list is remembered on your device between visits.

## Tech

Plain HTML, CSS, and JavaScript in a single `index.html` file — no build step, no framework, no server. The list of dinner options is saved in the browser's `localStorage`.

## Run locally

Just open `index.html` in any web browser, or serve the folder with any static file server, e.g.:

```bash
npx serve .
```

## Deploy

This is a static site, so it deploys as-is on Netlify (see `netlify.toml`), Vercel, GitHub Pages, or any static host.
