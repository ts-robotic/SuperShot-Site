# SuperShot Website

Official marketing website for **SuperShot**, the Windows screenshot and screen recording app.

**Live site:** [https://supershotapp.com](https://supershotapp.com)

## About SuperShot

SuperShot is developed by **TS Robotics** and solely licensed to **Mortgage Magick Limited**, trading as **Mortgage Magic**, for distribution. It is published in the Microsoft Store as **SuperShotAI** and is Windows-only.

## Tech

Pure static site. HTML, CSS and a few lines of vanilla JS. No build step, no dependencies.

- Self-hosted fonts: Clash Display (headings) and Satoshi (body), Indian Type Foundry via Fontshare, ITF Free Font Licence (`assets/fonts/FFL.txt`)
- Capture-overlay design system: selection marquee, corner handles, HUD readouts
- Scroll-reveal animation with full `prefers-reduced-motion` support
- SoftwareApplication and FAQPage structured data, `llms.txt`, sitemap

## Downloads referenced by the site

- **Microsoft Store (primary):** <https://apps.microsoft.com/detail/9PMD0JVXMS6T>
- **Direct installer (backup):** [SuperShot_2.0.0_x64-setup.exe](https://github.com/ts-robotic/supershot-windows/releases/download/v2.0.0/SuperShot_2.0.0_x64-setup.exe) from the `supershot-windows` releases

When a new Windows version ships, update the direct download URL, the version and size in the download card, and `softwareVersion` in the JSON-LD on `index.html`.

## Deploy

- **Production:** Cloudflare Pages project `supershot-site`, production branch `main`, custom domain `supershotapp.com`. Pushing to `main` deploys automatically.
- A legacy GitHub Pages workflow also publishes the repo (CNAME `supershot.tsrobotic.com`).

## Local preview

```bash
npx serve . -l 3000
```

Use an HTTP server rather than `file://` because asset paths are root-relative.

## Regenerating the social image

Open `assets/og-src.html` at exactly 1200 x 630 and screenshot it to `assets/og.png`.

---

Copyright (c) 2026 Mortgage Magick Limited. All rights reserved.
