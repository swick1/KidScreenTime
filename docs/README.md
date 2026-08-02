# Kid Screen Time — website

This folder is the marketing/landing site for Kid Screen Time. It's the only thing meant to be
published via GitHub Pages — nothing else in this repo should be served publicly.

## Files

| File | Purpose |
|---|---|
| `index.html` | The main landing page: what the app does, why it exists, screenshots, pricing, and a short FAQ. |
| `security.html` | The "what this app actually does to your PC" transparency page, linked from the main page's privacy section. |
| `license.html` | The full license text (TL;DR + legal text), linked from the main page's License section. Keep this in sync with the repo's top-level `LICENSE` file and `installer/license.txt` if it ever changes. |
| `screenshots/` | Real screenshots used on the landing page, captured directly from the running app. |

Plain HTML/CSS, no build step, no dependencies — open `index.html` directly in a browser to
preview changes locally.

## Hosting on GitHub Pages

1. In the repo's **Settings → Pages**, set the source to the `main` branch, `/docs` folder.
2. GitHub Pages serves everything under `docs/` at the repo's Pages URL, so this site ends up
   at `https://<username>.github.io/<repo>/website/`.
3. Any push to `main` that touches files under `docs/website/` updates the live site
   automatically within a minute or two — no separate deploy step.

## Updating

- **New release**: update the two "Download for Windows" links in `index.html` to point at the
  new GitHub release tag (currently
  `https://github.com/swick1/KidScreenTime/releases/tag/v1.0.0`).
- **New screenshots**: replace the files in `screenshots/` and keep the filenames referenced in
  `index.html` in sync, or update the `<img src="...">` paths if you rename them.
- **License changes**: update `installer/license.txt` (shown at install time), the repo's
  `LICENSE` file, and `license.html` together — all three should always say the same thing.
