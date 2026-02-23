# Cartulary

**A structured, temporal, offline-first worldbuilding and writing tool.**

*Your entire world in a single file. No cloud. No subscription. No compromises.*

---

## What Is This?

Cartulary is a desktop application for worldbuilders and writers. It treats your world as a queryable, visualizable, temporally-aware database — while giving you a writing environment where every name is a live link to your world's data.

Your characters, factions, locations, events, maps, and manuscripts all live in one portable file on your machine. Export everything, anytime, in formats you own.

## Why?

Every existing worldbuilding tool asks you to choose between structured data and creative freedom, between visualization and writing, between power and usability. Most are web apps that eat RAM, require subscriptions, and hold your creative work hostage behind login servers.

We looked at every option. They all share the same limitations: no structured data, poor visualization, no temporal awareness, and a disconnect between worldbuilding and writing.

Cartulary is built to fix that.

## What Makes It Different

### Your World Changes Over Time

Cartulary is built on **event sourcing**. Every change to your world is a dated event. Set the global year to 300 and see your world as it was. Set it to 500 and watch what changed. Borders shift on the map. Characters are born and die. Factions rise and fall. All queryable, all automatic.

No existing worldbuilding tool does temporal state reconstruction.

### Writing and Worldbuilding Feed Each Other

Write a scene — every entity name auto-links to your database. Hover a character to see their portrait and properties without leaving your prose. Invent a character mid-sentence and create the entity with one click. Record a battle scene as a world event. Rename an entity and every reference across all documents updates.

### Everything Connects

Typed, bidirectional relationships with properties. Interactive graph visualization. Maps with temporal geography. Timelines with custom calendars and causation chains. A visual query builder that lets you interrogate your world without writing SQL.

### Your Data, Your Rules

- Single `.cartulary` file (SQLite database — query it directly if you want)
- Export to JSON, Markdown, CSV, HTML static site, DOCX, PDF, ePub
- No lock-in. Not now, not ever.

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Shell | Tauri 2 (Rust backend, native OS webview) |
| Frontend | Svelte 5 + TypeScript |
| Database | SQLite (single portable file) |
| Rich Text | TipTap (ProseMirror) |
| Visualizations | Cytoscape.js, Leaflet, vis-timeline |

Targets: fast startup, proportional RAM usage, instant interactions once loaded. Built with Tauri and Rust — not Electron.

## Status

🚧 **Early development.** We're building the foundation: event-sourced data model, entity system, and core UI.

See the [Roadmap](./ROADMAP.md) for what's planned and where help is needed.

## Building From Source

### Prerequisites

- [Rust](https://rustup.rs/) (latest stable)
- [Node.js](https://nodejs.org/) (LTS)
- System dependencies for Tauri:
  - **Linux:** `libwebkit2gtk-4.1-dev libgtk-3-dev libayatana-appindicator3-dev librsvg2-dev libssl-dev libsoup-3.0-dev libjavascriptcoregtk-4.1-dev patchelf`
  - **Windows:** Visual Studio Build Tools with C++ workload + WebView2 Runtime
  - **macOS:** Xcode Command Line Tools

### Build & Run

```bash
git clone https://github.com/cartulary-app/cartulary.git
cd cartulary
npm install
cargo tauri dev
```

First build compiles all Rust dependencies (~2-5 minutes). Subsequent builds are fast.

## Contributing

Cartulary is in its earliest stages. If the vision resonates with you, here's where help matters most:

- **Rust** — Event sourcing engine, SQLite layer, auto-linking index
- **Svelte/TypeScript** — Entity editor, rich text integration, visualization views
- **Worldbuilders** — Feature feedback, schema templates, testing with real worlds
- **Designers** — UI/UX, themes, icons, cartographic assets
- **Translators** — Interface localization (i18n built in from day one)

Open an issue to discuss before submitting large PRs. Read the [Vision Document](https://cartulary.app) for the full picture of where this is headed.

## License

[GPL-3.0](./LICENSE)

Source-available. Pre-built binaries will be available as a one-time purchase. Free to compile from source, always.

---

*Cartulary: a medieval manuscript register. A structured record of everything that matters.*
