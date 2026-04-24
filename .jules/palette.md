## 2026-04-22 - Improved Alt Text for Dynamic Content (Typing SVG)

**Learning:** Screen readers cannot parse the text content drawn within SVGs via APIs (e.g., readme-typing-svg) when generic alt text like "Typing SVG" is used. The text is rendered visually but remains inaccessible.
**Action:** Always extract the actual text strings passed in the URL parameters (e.g., `lines=...`) and use them as explicit, descriptive alt text to ensure the animated content is accessible to assistive technologies.

## 2024-05-24 - False Affordances & Badge Contrast

**Learning:** Found two interesting UX patterns in profile readmes: 1) Generated header graphics are often wrapped in links to the generator repo by default, creating a false affordance where users expect to go to a project/profile but instead go to a tool repo. 2) Default brand colors on shields.io badges (like ChatGPT's teal #74aa9c) often fail WCAG contrast requirements (2.63:1) when used with white text/logos.
**Action:** Always check default link wrapping on generator components and remove them if they don't serve the user's navigational intent. When using brand colors for badges, verify contrast ratios and don't be afraid to darken the brand color (like to #0A6650, achieving 6.9:1) to prioritize accessibility over strict brand adherence.

## 2024-05-24 - Accessible Names for Image-Only Links

**Learning:** When an image is the sole content of a link (like a repository card or a social badge), its `alt` text serves as the accessible name for the entire link. Screen reader users need to know where the link goes, not what the image looks like. Furthermore, if a link opens in a new tab (`target="_blank"`), this behavior should be communicated in the accessible name.
**Action:** Always ensure the `alt` text for image-only links describes the destination (e.g., "YouTube Downloader repository") rather than the visual appearance (e.g., "YouTube Downloader Readme Card"). Additionally, append warnings like "(opens in a new tab)" to the `alt` text if the link exhibits that behavior, especially in Markdown where `aria-` attributes are not available to provide this context separately.
