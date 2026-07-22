# Brechtland — Website Portfolio

Live website demos for auto detailing, ceramic coating, window tint and wrap shops.

**Live at:** https://portfolio.brechtland.com

Built and maintained by [Brechtland LLC](https://brechtland.com) · tyler@brechtland.com

---

## What's here

| Folder | Demo | Focus |
|---|---|---|
| `signature/` | Brechtland Signature | Flagship — video hero, before/after, live map |
| `velocity/` | Velocity Wraps | Vinyl wraps & PPF |
| `apex/` | Apex Tint Studio | Window tint + shade picker |
| `fast-exotic/` | Fast Exotic Detailing | Exotic / dark editorial |
| `lakeshore/` | Lakeshore Auto Pros | PPF, tint, multi-location |
| `meridian/` | Meridian Detail Atelier | Quiet-luxury / collector |
| `evergreen/` | Evergreen Eco Detailing | Steam & eco-friendly |
| `stateline/` | Stateline Restorations | Scroll-cinematic restoration |

All demo content is placeholder — real builds use the client's own photos, services and pricing.

**Every form on these demos is disabled.** Submitting shows a demo notice and sends nothing;
there are no live form endpoints anywhere in this repo.

---

## Rebuilding after a template change

These folders are generated from the master templates in the Brechtland Studio app
(`Website Templates\templates\`). Don't hand-edit the demos here — edit the master
template, then regenerate, so the app and the portfolio never drift apart.

For each template:

1. Copy the template folder's contents into its portfolio folder (everything **except**
   `template.html` and `manifest.json`).
2. Copy `template.html` → `index.html` (the rename is what gives clean URLs like
   `/signature/` instead of `/signature/template.html`).
3. Replace any `https://formspree.io/f/...` endpoint with `#demo`.
4. Paste the demo-mode block (form blocker + "All templates" back link) directly before
   `</body>`. Copy it from any existing demo — search for `bl-demo-ov`.

Then commit and push; GitHub Pages redeploys in about a minute.

---

## Hosting notes

- **GitHub Pages**, served from the `main` branch root.
- `CNAME` points the site at `portfolio.brechtland.com` — don't delete it, Pages
  resets the custom domain without it.
- `.nojekyll` disables Jekyll processing so every file publishes as-is.
- Repo is ~183 MB (mostly hero video), well under the 1 GB Pages limit.
