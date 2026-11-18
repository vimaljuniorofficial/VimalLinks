# Vimal Links

A single-file editorial link-in-bio website and private Admin Studio built inside `index.html`, styled in an Editorial Monograph layout with Paper Light and Nocturne Dark themes.

## Features

- **Public Link Directory:** Clean responsive layout featuring a profile portrait, bio, verified seal toggle, social icon grid, share/copy actions, and light/dark theme switcher.
- **Automatic Website Favicons:** Resolves website favicons dynamically across multiple fallback sources (including custom TLDs and inline SVG favicons) with session caching and clean icon fallback for non-web links.
- **Hidden Admin Studio (`/#admin`):** No admin button or link is shown on the public page. Navigate directly to `/#admin` to manage:
  - Profile display name, bio, portrait upload/reset, verified badge, accent colors, and default theme
  - Link directory items (add, edit, enable/disable, drag-and-drop or arrow reordering, delete)
  - Social profile links
  - Admin password update
  - JSON backup export, import, and full reset
- **Mobile Responsive:** Two-column editorial spread on desktop and centered single-column layout on mobile viewports.

## Local Development

```bash
npm install
npm run dev
```

Open `http://localhost:3000` for the public page and `http://localhost:3000/#admin` for the Admin Studio.

## Build

```bash
npm run build
```

Outputs the production bundle to `dist/`.

## Deploy on Vercel

This repository includes `vercel.json` preconfigured for Vite (`npm run build` -> `dist`).

### Option 1: GitHub + Vercel Dashboard
1. Push this repository to GitHub.
2. Import the repository at [vercel.com/new](https://vercel.com/new).
3. Click **Deploy** (build settings are detected automatically from `vercel.json`).

### Option 2: Vercel CLI
```bash
npx vercel --prod
```

## Data Persistence & Migration

All profile settings, links, and theme preferences are stored in browser `localStorage`. When moving between environments (such as preview to a custom domain), open `/#admin` and use **Export JSON** and **Import JSON** under **Security & Backup** to transfer your configuration.
