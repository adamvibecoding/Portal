# Portal

Personal bookmark portal — Apple-style, single-file, Vercel-deployed.

**Live:** https://portal-adamvibecoding.vercel.app

---

## Stack

- `index.html` — all CSS, JS, and data in one file
- `fonts/` — SF Pro Display & Text (.otf, extracted from Apple's SF-Pro.dmg)
- Vercel — auto-deploys on push to `main`

---

## Adding or editing links

All data lives in `window.PORTAL_DATA` inside `index.html`. Edit that object and push.

**Card fields:**
```js
{ "name": "Linear", "url": "https://linear.app", "slug": "linear", "color": "5E6AD2", "description": "Issue tracking." }
```

- `slug` — simpleicons.org slug for the brand icon
- `color` — hex without `#`

**AlphaSeek stack chips:**
```js
{ "label": "Vercel", "url": "https://vercel.com/...", "slug": "vercel" }
```

Push → Vercel deploys in ~30 seconds.

---

## Local preview

Double-click `index.html` — data is inlined so it works on `file://`.

---

## Fonts

SF Pro fonts are in `fonts/`. If you need to re-extract them from `SF-Pro.dmg`:

```
# Extract with 7-Zip (4-layer nested archive)
7z x SF-Pro.dmg
7z x 2.hfs
7z x SF\ Pro\ Fonts.pkg
7z x Payload
# .otf files appear in Library/Fonts/
```

Copy `SF-Pro-Display-Regular.otf`, `SF-Pro-Display-Semibold.otf`, `SF-Pro-Text-Regular.otf` into `fonts/`.
