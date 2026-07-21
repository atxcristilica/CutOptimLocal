# CutOptim Local

An offline, browser-based cutting-layout optimizer for panels, sheets, bars and pipes. Minimizes material waste and cost by testing multiple packing strategies across all available stock sizes. Runs entirely in your browser — nothing leaves your device.

## Features

- **2D panel nesting** (sheets/boards/glass) and **1D linear cutting** (bars/pipes/profiles)
- **Multi-strategy optimization** — tries several sort orders, guillotine split heuristics, and per-stock preferences, then ranks them so you can pick the best or compare alternatives
- **Uses all available stock sizes** and mixes them intelligently to minimize waste
- **Cost-aware** — enter a price per m² (2D) or per linear meter (1D) and the optimizer ranks options by total cost, with a full price breakdown
- **Kerf** (blade width), **rotation** control, and **grain-lock** per part
- **Visual SVG layouts** plus a cut-list table and a printable/PDF report
- **CSV import/export** of parts, and **project save/load** as JSON
- **Installable PWA** — works offline and can be added to a phone's home screen (when hosted over HTTPS)

## Usage

Open `index.html` in any modern browser — no install, no server, no build step required.

For the installable/offline (PWA) features, the app must be served over `http(s)://` (for example via GitHub Pages), since browsers disable Service Workers on `file://` URLs. Opening the file directly still gives you the full optimizer, just without the install/offline extras.

## Notes

- The optimizer uses heuristic (guillotine best-fit) nesting — fast and near-optimal, but not a guaranteed global optimum.
- Kerf is reserved conservatively after each part, so real-world waste is often slightly lower than reported.
