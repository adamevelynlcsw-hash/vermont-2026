# Vermont ski week (Dec 26, 2026 to Jan 1, 2027)

A phone-friendly portal for the family. Wanderlog is the planning tool; this page is the easy-to-read copy.

Live site: https://adamevelynlcsw-hash.github.io/vermont-2026/

## How it works

- Everything is in `index.html`. No build step.
- All trip content sits in the `TRIP` data block at the top of the file (`<script id="trip-data">`). Design and code are below it.
- Photos are Wikipedia lead images, fetched by each visitor's browser and linked back to their article. Restaurants have no photo; their card links to Google Maps for photos and menus.
- The page asks search engines not to index it (`noindex`). A public repo is still public, so keep private details out.

## Updating from a new Wanderlog export

1. Export the plan from Wanderlog (it carries its own date).
2. Open the Vermont Ski Trip project in Claude, attach the export, and paste `UPDATE_PROMPT.md`.
3. Claude edits the `TRIP` block, bumps `updated`, pushes here, and reports any conflicts.

Manual edit: change the `TRIP` block in `index.html` on github.com and commit. Pages redeploys in about a minute.

## Never put in this repo

Last names, confirmation or loyalty numbers, traveler emails or phone numbers, health notes.

## Data conventions

- `status`: `confirmed`, `optional`, `backup` (shown as a green circle, blue square, black diamond).
- `src`: `plan` (from the Wanderlog export) or `extra` (curated idea, not committed).
- `hours`: seven strings, Sunday first. Use `"Closed"` for closed days. Leave `hours` off when not listed.
- `warn` on a day item shows a "Heads up" note (closed that day, sources disagree).
- `wiki`: exact English Wikipedia article title used for the photo.
- Food picker: each day has `eat`, a curated list of `{ id, meal, note, top }` pointing at food places, and an optional `eatNote` heads-up. The page builds the town filter from those places. Mark one pick per day `top: true`, and only list places not known to be closed that date.
- Food places can carry `kind` (`sit`, `quick`, `shop`, `brew`), `order` (what to get) and `fl: true` (a New England name not found in Florida).
