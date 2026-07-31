# Detroit Craft Club — Vue

A Vue 3 + Vite site. Three pages (Home, Events, About) with shared nav + footer.

## Run it

```bash
cd detroit-craft-club-site
npm install
npm run dev
```

Then open the URL Vite prints.

## Where things live

- `src/data.js` — all event and admin content. Edit here to change what's on the pages.
- `src/views/` — one file per page: `Home.vue`, `About.vue`, `Events.vue`.
- `src/components/` — `NavBar.vue` and `SiteFooter.vue` (shared across pages).
- `src/styles.css` — global resets, fonts, and mobile breakpoints.
- `src/main.js` — router setup.

## Build for production

```bash
npm run build      # outputs to dist/
npm run preview    # preview the build
```

## Brand colors

- Deep teal `#274249`
- Sage green `#759A79`
- Pale yellow `#FDF8E9`
- Pale sage `#E4ECE0`
- Rust accent `#C1714A`
