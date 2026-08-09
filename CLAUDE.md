# Itin Wireframe

A clickable wireframe (not production code) for "Itin," a trip-itinerary app. Demonstrates interactions for developer handoff — see `Itin Wireframe - Developer Handoff.docx` for the written spec.

**Everything lives in one file: `index.html` (~2,400 lines — CSS lines 1–536, HTML lines 538–1311, JS lines 1312–2383).** Plain HTML/CSS/JS, no build step, no framework. External libs via CDN: Leaflet (maps), SortableJS (drag-to-reorder), Google Fonts (Cal Sans, Instrument Serif, Courier Prime).

**Do not read the whole file to make a small change.** Use the section index below to jump straight to the relevant line range with `sed -n 'START,ENDp' index.html` or the Read tool's offset/limit params.

## Local dev
```
python3 -m http.server 4173 --directory .
```
Then open `localhost:4173`. **Never deploy to Vercel unless Ryan explicitly says so in the moment** — he iterates locally and controls when changes go live on the shared `itin-wireframe.vercel.app` link.

## Section index

### CSS (lines 1–536)
| Section | Line |
|---|---|
| Header comment (working interactions list) | 13 |
| Palette system (paintbrush customizer) | 91 |
| Itin font options | 136 |
| Home | 172 |
| Trip hero | 204 |
| Days nav | 225 |
| Day sections | 231 |
| Element cards | 241 |
| Element meta chips | 264 |
| Edit element sheet | 274 |
| Trip search + filter | 290 |
| Photo strips / tiles | 303 |
| Photo lightbox | 323 |
| Add button | 337 |
| Day notes | 342 |
| Toast | 349 |
| Invite / participant picker sheet | 353 |
| Customize (palette) sheet | 384 |
| Filter sheet | 403 |
| Add-element type picker | 413 |
| Trip map view | 422 |
| Explore (compass) tab | 443 |
| Saved (star) tab | 469 |
| Profile (person) tab | 483 |
| New itin create screen | 501 |
| Legend | 527 |

### HTML (lines 538–1311)
| Section | Line |
|---|---|
| Home screen | 546 |
| Trip / day view | 633 |
| Caucasus trip (blank) | 878 |
| Profile screen | 1020 |
| Saved (star) screen | 1052 |
| New itin create screen | 1072 |
| Explore (compass) screen | 1121 |
| Trip map view | 1140 |

### JS (lines 1312–2383)
| Section | Line |
|---|---|
| Screen + day navigation | 1313 |
| Sliding nav highlight | 1328 |
| Sticky day bar / scroll-spy | 1367 |
| Toast | 1390 |
| Heart (Want to go) + Star (Favorites) toggles | 1399 |
| Tap-to-copy confirmation # | 1423 |
| Tap element card to edit (bottom sheet) | 1433 |
| Search + filters (Home) | 1538 |
| Add element (inline, nameable) | 1587 |
| Invite / share bottom sheet | 1593 |
| Clipboard helper | 1612 |
| Drag-to-reorder within day | 1624 |
| Add-element type picker | 1625 |
| Element meta chips | 1678 |
| Photo lightbox | 1750 |
| Trip search + filter (trip view) | 1785 |
| Day notes (auto-grow textarea) | 1808 |
| Explore (compass) map | 1878 |
| Profile | 1959 |
| Saved (favorited published itins) | 1974 |
| New itin create | 2018 |
| Customize itin: palette picker | 2096 |
| Trip map (pins + route) | 2240 |

## Other files
- `index.html.bak` — a manual point-in-time backup Ryan made. Stale by definition; don't read it for current state and don't edit it.
- `Photos/` — profile/avatar source images referenced by the wireframe.
- `Itin Wireframe - Developer Handoff.docx` — the written spec for developer handoff.

## Workflow
- This is a git repo (local only, no remote). After edits, check `git diff` instead of re-reading the whole file to confirm what changed.
- Line numbers above will drift as the file is edited — re-grep the section markers (`/* SECTION */`, `<!-- SECTION -->`, `// --- Section ---`) if a line number looks off, rather than assuming it's still exact.
