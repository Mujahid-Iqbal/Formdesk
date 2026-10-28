# Formdesk

A Next.js App Router application for a furniture configurator business. React renders the sales page and desk studio; Three.js provides the browser-only 3D previews. No backend, payment collection or live lead delivery is connected.

## Run locally

Requires Node.js 22.13 or later.

```sh
npm ci
npm run dev
```

Open http://127.0.0.1:4173. The routes are `/` (sales page) and `/studio/` (configurator).

## Build and preview

```sh
npm run build
npm run preview
```

Next.js exports production HTML, CSS and JavaScript into `out/`. The existing Sites project serves that output using `.openai/hosting.json`. It preserves owner-private access. `out/`, `.next/` and `node_modules/` are ignored; dependencies are pinned in `package-lock.json`.

The application currently uses `output: 'export'`. Server actions, request-dependent API routes and database-backed features require a server deployment or separate API when added.

## Source

- `app/layout.jsx`: root document and metadata.
- `app/page.jsx`, `app/SalesPage.jsx`, `app/sales.css`: branded sales page.
- `app/studio/page.jsx`, `app/studio/DeskStudio.jsx`, `app/studio/studio.css`: desk studio.
- `lib/sales.js`, `lib/studio.js`: browser-only Three.js initialization and interaction code, mounted via React effects with renderer, event and animation cleanup.
- `public/pilot-brief.txt`: proposed $500 pilot scope, exclusions and acceptance checks.
- `sales-kit/prospects.html`: local owner sales kit with ten prospects, sources, qualification notes and unsent outreach drafts. It stays outside the deployed static output. Run `python3 sales-kit/build-kit.py` to regenerate the report.

The studio supports procedural geometry, grain textures, size and finish controls, optional accessories, illustrative USD prices, PNG export, browser-local save/restore and downloadable quote briefs. Google Fonts is optional; system fonts provide a fallback. Screenshots are concept illustrations, not client projects.

## Before outreach

Configure a business contact email and prospect access. The current sales page downloads the pilot offer without submitting an enquiry; the studio downloads customer details locally. Replace the generic product and pricing with maker-approved specifications before selling a pilot, then implement and verify the agreed email delivery provider and data collection notice.
