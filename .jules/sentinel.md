## 2024-05-24 - Deprecated Service Links in Documentation

**Vulnerability:** Use of deprecated URL shorteners (git.io) and application domains (herokuapp.com) in `README.md`.
**Learning:** Abandoned domains or services like Heroku free-tier apps can be claimed by malicious actors (subdomain takeover), allowing them to serve malicious content (e.g., tracking pixels or phishing) to users viewing the documentation.
**Prevention:** Always use direct links to official, actively maintained domains. Regularly audit and update external URLs and embedded assets in documentation.
