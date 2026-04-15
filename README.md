# Countries Visited

An interactive world map for tracking countries you've visited. Click countries on the map or use the checkbox list to mark them visited.

## Features

- **Interactive map** — click any country to toggle visited status, with zoom and pan support
- **Shareable URLs** — your visited countries are encoded in the URL, so you can share your map with anyone
- **Persistent storage** — state is saved to `localStorage` and synced to the URL on every change
- **Country grid** — scrollable checkbox list of all countries with search/filter
- **Stats** — live count of visited countries, total, and percentage complete
- **Resizable panel** — drag the handle between the map and country list to adjust the split

## Usage

Open `index.html` directly in a browser — no build step or server required.

```
open index.html
```

### Marking countries

- **Map**: click a country to toggle it visited/unvisited
- **List**: check/uncheck any country in the grid at the bottom
- **Search**: type in the search box to filter the country list

### Sharing

Copy the URL from your browser after marking countries — the `?=` query parameter encodes your full visited set as a compact bitmask. Anyone opening that URL will see your map.

### Controls

| Control | Action |
|---|---|
| Click country | Toggle visited |
| Scroll / pinch | Zoom |
| Click + drag | Pan |
| `+` / `−` buttons | Zoom in / out |
| `⌂` button | Reset view |
| Clear all | Remove all visited marks |

## Tech

- [D3.js v7](https://d3js.org/) — map rendering and zoom
- [TopoJSON](https://github.com/topojson/topojson) — geographic data
- [world-atlas](https://github.com/topojson/world-atlas) — 50m resolution country shapes
- Vanilla JS, no framework, no build tooling — single `index.html` file
