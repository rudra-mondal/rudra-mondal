## 2026-04-22 - Improved Alt Text for Dynamic Content (Typing SVG)

**Learning:** Screen readers cannot parse the text content drawn within SVGs via APIs (e.g., readme-typing-svg) when generic alt text like "Typing SVG" is used. The text is rendered visually but remains inaccessible.
**Action:** Always extract the actual text strings passed in the URL parameters (e.g., `lines=...`) and use them as explicit, descriptive alt text to ensure the animated content is accessible to assistive technologies.
