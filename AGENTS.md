# AGENTS.md

## Project architecture

This is a static, single-page app with no backend and no build step:

- `index.html` — the entire application: markup, styles, and logic all in one file.
- `netlify.toml` — tells Netlify to publish the repo root as-is (no build command).

There is no server, no framework, and no bundler. Do not introduce one unless the scope of the app changes significantly (e.g. adding multi-user sync).

## Data persistence

The list of dinner options is stored client-side in `localStorage` under the key `dinnerOptions`. There is no database and no server-side storage — each visitor has their own independent list, and it only persists on the device/browser they used.

If a future feature requires shared or server-side state (e.g. a household voting on dinner together), that would need Netlify Database or Netlify Blobs — see the project's `general-database` guidance before adding one.

## Conventions

- Keep everything in `index.html` unless the app grows enough to justify splitting into separate CSS/JS files.
- Prefer small, dependency-free JavaScript over adding libraries.
- Style variables are defined as CSS custom properties at the top of the `<style>` block — reuse them rather than hardcoding new colors.
