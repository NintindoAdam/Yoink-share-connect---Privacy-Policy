# Yoink — privacy & support site

Two static pages for GitHub Pages. No build step, no dependencies.

- `index.html` — landing page (use this as your **Support URL** in App Store Connect)
- `privacy.html` — privacy policy (use this as your **Privacy Policy URL**)

## Before you upload — 2 swaps

Search-and-replace in BOTH files:

1. `REPLACE_WITH_YOUR_EMAIL@example.com` → your real support email
   (appears in `index.html` once and `privacy.html` once)
2. If you rename the app away from "Yoink", replace "Yoink" throughout both files
   with the final name.

## Upload to GitHub Pages

1. Create a new public repo, e.g. `yoink-privacy`.
2. Upload `index.html`, `privacy.html`, and this README (drag them into the repo
   on github.com, or push from the terminal).
3. In the repo: **Settings → Pages → Source: Deploy from a branch → main → /(root) → Save**.
4. Wait ~1 minute. Your site is live at:
   `https://YOUR_USERNAME.github.io/yoink-privacy/`
   - Privacy policy: `https://YOUR_USERNAME.github.io/yoink-privacy/privacy.html`

## Put the URLs in place

- **In the app:** replace the placeholder `https://yoink.app/privacy` in
  `SettingsView.swift` (~line 399) with your live `privacy.html` URL.
- **In App Store Connect:** Privacy Policy URL = the `privacy.html` link;
  Support URL = the `index.html` (root) link.
