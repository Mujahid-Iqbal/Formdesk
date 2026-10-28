# Formdesk
A buildless furniture configurator demo. Serve `dist/` over HTTP (`python3 -m http.server 4173 --directory dist`).

Self-hosted Three.js powers the procedural desk, material textures, lighting and pointer orbit controls. Dimensions, finishes, frame color and accessories update both geometry and illustrative USD pricing. Supports PNG export, browser-local save/restore and a downloadable customer quote brief. No backend, payment collection or lead submission is connected. Google Fonts is optional; system fonts provide a fallback.

Prices are demo assumptions. Before selling: replace pricing and product constraints with a furniture maker's specifications, connect an approved lead endpoint and transactional email, configure merchant branding, and validate manufacturing dimensions.

## Sales page and pilot offer
The root now contains the branded sales page; `/studio/` preserves the original configurator. `dist/pilot-brief.txt` specifies the proposed $500 pilot and acceptance checks. The landing page downloads the brief without submitting leads; configure a business contact route before outreach. Existing Site access remains private.

`sales-kit/prospects.html` is the owner-only local sales kit with ten researched prospects, source/contact links, qualification notes and individual unsent message drafts. It is deliberately outside `dist/` and is not published. `prospects.json` stores the same structured research; `build-kit.py` regenerates the report.
