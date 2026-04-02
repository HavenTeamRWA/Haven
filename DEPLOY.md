# Haven GitBook — Deployment Guide

This folder contains the complete GitBook documentation source for Haven AI Yield.

---

## File Structure

```
haven-gitbook/
├── README.md                      ← Landing page (shown at root URL)
├── SUMMARY.md                     ← Navigation structure (required by GitBook)
├── book.json                      ← GitBook config
├── getting-started/
│   ├── overview.md
│   ├── quickstart.md
│   └── architecture.md
├── core-products/
│   ├── havenclaw.md
│   ├── havenscore.md
│   ├── havenskill.md
│   └── gateway.md
├── integration/
│   ├── openclaw.md
│   └── api.md
└── resources/
    ├── roadmap.md
    └── faq.md
```

---

## Deployment Steps

### Option A — GitBook.com (Recommended, easiest)

1. Push this folder to a GitHub repository (e.g. `haven-ai/docs`)
2. Go to [gitbook.com](https://www.gitbook.com) and create an account
3. Create a new Space → choose **Import from GitHub**
4. Select the repo and set the root path to this folder
5. GitBook will auto-sync. Every push to `main` updates the docs live.

### Option B — Self-hosted with GitBook CLI

```bash
# Install GitBook CLI
npm install -g gitbook-cli

# Enter the folder
cd haven-gitbook

# Install dependencies
gitbook install

# Preview locally
gitbook serve
# → Opens at http://localhost:4000

# Build static site
gitbook build
# → Outputs to _book/ folder, deploy anywhere (Vercel, Nginx, S3, etc.)
```

### Option C — Deploy static build to Vercel

```bash
gitbook build
cd _book
vercel deploy
```

---

## Editing Content

All pages are standard Markdown. Edit any `.md` file and push — changes reflect immediately if using GitBook.com sync.

The `SUMMARY.md` file controls the sidebar navigation. To add a new page:
1. Create the `.md` file in the appropriate folder
2. Add a line to `SUMMARY.md` pointing to it

---

## GitBook Special Syntax Used

```
{% hint style="info" %}   ← Blue info callout
{% hint style="warning" %} ← Yellow warning callout
{% endhint %}
```

These render as styled callout boxes in GitBook. They will appear as plain text in standard Markdown viewers — that's expected.
