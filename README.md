# Nexus Lite

A lightweight personal bookmark dashboard. No accounts, no setup, no server — just open the file and go. Everything saves to your browser's localStorage.

![Theme](https://img.shields.io/badge/theme-dark%20%2F%20light-c8a96e) ![Storage](https://img.shields.io/badge/storage-localStorage-7eb8c9) ![Dependencies](https://img.shields.io/badge/dependencies-none-6ec98a) ![Mobile](https://img.shields.io/badge/layout-responsive-c96eb4)

---

## Features

### Bookmarks
- **Collapsible categories** — color-coded accents, favicons, instant search
- **Pinned category** — pin one category to the top as a permanent anchor
- **Category colors** — 30-color curated palette, pick while renaming
- **Inline editing** — add, edit, delete links and categories without touching code
- **Move links** — reassign any link to a different category via the edit modal
- **Drag-and-drop reordering** — drag categories and links into any order
- **Alphabetical sort** — sort everything A–Z in one click
- **Global quick-add** — add a link from the header without opening a category first

### Import & Export
- **Browser import** — import from Safari or Firefox HTML exports with full preview: rename categories, merge into existing ones, skip duplicates
- **Export** — download a `nexus-lite-bookmarks.json` backup any time

### Sidebar
- **Scratch pad** — quick notes, auto-saved to localStorage
- **RSS feeds** — up to 10 feeds, combined chronological view, 7-day filter, per-feed filtering, inline rename, drag-to-reorder

### General
- **Theme switcher** — warm dark and parchment light modes
- **Responsive layout** — works on desktop, tablet, and mobile
- **Single file** — one `index.html`, no build tools, no frameworks, no backend

---

## Setup

No setup required. Open `index.html` in any browser and start adding bookmarks.

To host it online, upload to any static host — GitHub Pages, Netlify, Cloudflare Pages, or even a basic web server. No configuration needed.

---

## Data & Portability

All data is stored in your browser's localStorage under the key `nexus_lite_data`. Use the **Export** button any time to download a JSON backup.

The format is simple and human-readable:

```json
{
  "categories": [
    {
      "id": "x1a2b3c",
      "name": "Favorites",
      "open": true,
      "pinned": true,
      "color": "#c8a96e",
      "links": [
        { "id": "x4d5e6f", "name": "Example", "url": "https://example.com" }
      ]
    }
  ]
}
```

---

## Importing Bookmarks

Click **Import** in the header and drop your browser's bookmark export file:

- **Safari:** File → Export Bookmarks
- **Firefox:** Bookmarks → Manage Bookmarks → Import and Backup → Export Bookmarks to HTML

The import preview lets you rename categories, merge them into existing ones, and skip duplicates before committing anything.

---

## RSS Feeds

Add up to 10 feeds via the **Edit** button in the RSS panel. Feed names are auto-generated from the hostname and can be renamed inline. Click a feed name to filter to that feed; click again to return to the combined view.

---

## Difference from Nexus (full version)

| Feature | Nexus Lite | Nexus |
|---|---|---|
| Bookmark management | ✓ | ✓ |
| RSS feeds | ✓ | ✓ |
| Scratch pad | ✓ | ✓ |
| Import / Export | ✓ | ✓ |
| Writing prompt | ✓ | ✓ |
| Web search panel | — | ✓ |
| Fidget widget | — | ✓ |
| GitHub sync | — | ✓ |
| Cross-device sync | — | ✓ |

Nexus Lite is ideal for local use or sharing with others who want a simple, self-contained dashboard with no configuration.

---

## Stack

No frameworks. No build step. No package manager.

- Vanilla HTML, CSS, JavaScript
- [Syne](https://fonts.google.com/specimen/Syne) + [Inconsolata](https://fonts.google.com/specimen/Inconsolata) via Google Fonts
- [rss2json](https://rss2json.com) + [corsproxy.io](https://corsproxy.io) as CORS proxies for RSS feeds

---

*Built with [Claude](https://claude.ai) — AI-assisted development at its finest.*
