## 2026-04-04 - Heroku vs Edge-Cached SVG Generators

**Learning:** External SVGs hosted on Heroku for GitHub Profile READMEs often suffer from slow routing, cold starts, and potential timeout errors from GitHub's Camo proxy.
**Action:** Replace `herokuapp.com` with `demolab.com` (e.g., for `readme-typing-svg` and `github-readme-streak-stats`) which utilizes Cloudflare/Vercel edge caching to render SVG images faster and avoid timeout errors.
