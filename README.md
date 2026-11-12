# Multi-Route Profile Comparison (路線剖面比較)

Put the distance–elevation profiles of several hiking routes on one chart and save it as A4 portrait or landscape JPG pages at 300 dpi.

**Live demo:** https://shainyhsu.github.io/multi-route-profile-comparison/

## Features

- Load any number of GPX, KML or KMZ files; the chart draws the top 10 (each route can also be left off the chart). The first is the main route, shaded by grade every 100 m; drag a route by its handle to reorder the list or make it the main route
- Vertical axis is the elevation relative to the start: every line begins at 0 km and 0 m, so the chart compares steepness and length; actual elevations are written next to the place names (start, high point and end of the main route, end of every other route)
- Elevations come straight from each GPX file; only points without elevation data are filled in from the Ministry of the Interior’s 20 m digital terrain model (Taiwan)
- High-contrast line colors for screens, plus a distinct dash pattern for every comparison line so the chart still reads on a black-and-white laser printer; light colors get a dark outline, lines get a white edge where they cross the grade bands, and labels over the bands sit in framed boxes
- Save link or .json file to move everything to another device
- Live profile editor: tap a line to trim before or after a spot, add a point, rename a point and see its elevation; slide sideways to move along the line
- Print layout: true-scale (1:1) profile, elevation profile with pack-load spans, legend, route notes, grade bands with pack loads, and a distance-by-grade table with the steepest 300 m and 1 km
- A4 at 300 dpi (portrait 2,480 × 3,508 px, landscape 3,508 × 2,480 px) with 10 mm print margins; the landscape profile spans the full page width; longer content continues onto additional pages
- Per route: section by waypoint or km, reverse, scale to the posted trail distance, names and short name, line color and style, pack load (full pack or daypack), grade-table option, notes, and which points to mark
- Traditional Chinese / English interface (English uses official or established English place names and American usage); light/dark page (dark by default, shared with the other tools); the card itself is always light for printing and sharing
- Two-column page layout on laptops and desktops

## How to use

1. Open the link above (fully client-side; files are not uploaded to a server)
2. Add GPX or KML files, or try the sample
3. Adjust each route and the card settings
4. Download the JPG pages, or share them from a phone

## Tech

Single HTML page on GitHub Pages. No backend, no install. Terrain data: Ministry of the Interior 20 m grid digital terrain model; tiles converted by OsmHackTW terrain-rgb in 2023, released under the Open Government Data License (https://data.gov.tw/license).

## License

Copyright (c) 2026 Shainy Hsu. All rights reserved. See [LICENSE](LICENSE).

## Version history

Newest first. Times are Taiwan time (UTC+8). Also kept in [CHANGELOG.md](CHANGELOG.md).

- V12 | 2026-11-12 19:30 | Mirror option next to Reverse: the route comes back the same way, so the line ends where it started and named points show on the way out and back; on phones the docked profile editor now always opens expanded
- V11 | 2026-11-11 16:55 | Card legend now lists every route (main route first), each with a length bar under it on the same km scale as the profile, showing the pack load; the span arrows above the elevation profile are gone
- V10 | 2026-11-11 16:40 | Reverse now swaps the start and end names on every route (typed names and named points), and a route named like "A-B" or "A→B" becomes "B-A"; an end with no name is labeled Destination (目的) instead of the route name
- V9 | 2026-11-11 16:20 | Notes moved to a ? button in the header, next to Save; each route's settings now end with a Collapse button, so you don't have to scroll back up to close them
- V8 | 2026-11-11 11:45 | Pasting a save link into a tab that already has the page open now loads it too (before, only a fresh open did)
- V7 | 2026-11-11 11:25 | Save links are now short (about 90 characters): the save is encrypted in your browser, only the scrambled copy is stored online, and the key stays in the link, so whoever has the link can open it without signing in; the full link is used if the short one can't be made
- V6 | 2026-11-11 10:07 | New license terms: free to use in a browser for personal, work, school or club use, and the results you make are yours to share; copying, paid services built on it, and AI training need written permission. A License link sits at the bottom of the page
- V5 | 2026-11-11 09:15 | Save button: share or copy a save link, or download and open a .json file, to move the routes and settings to another device (it still autosaves in the browser)
- V4 | 2026-11-10 23:15 | Trim right at a named point (the point becomes the new start or end); sliding along a line no longer snaps back to nearby points; Duplicate button adds the same GPX again so each copy can be trimmed to its own section, starting from 0 km
- V3 | 2026-11-10 10:40 | Live profile editor above the card: tap any line to trim the part before or after that spot, add a named point, rename or hide a point, and read its elevation; card settings and preview merged into one panel; on a phone or tablet held upright the editor is docked at the bottom (with Hide) so it stays in view while editing routes
- V2 | 2026-11-10 09:35 | Route limit raised: add more than 10 GPX files and the chart draws the top 10 (with a per-route Show on the chart option); the sample routes make way for the first files you add; drag routes by the numbered handle to reorder or change the main route; three more line colors and dash styles for 10 lines
- V1 | 2026-11-10 07:51 | First version: up to 7 GPX/KML routes on one profile, elevation relative to the start with actual elevations next to place names, GPX elevations with DTM filling gaps, high-contrast colors plus dash patterns for black-and-white printing, 1:1 profile, grade bands with pack loads, distance-by-grade table, A4 portrait/landscape JPG at 300 dpi with additional pages when needed, Chinese/English, light/dark page
