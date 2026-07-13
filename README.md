# Central London Submarkets

Open `index.html` in a web browser to explore the Central London office occupier guide. Desktop users can hover over the map for Grade A and Grade B prime rents and select a submarket to open its linked dashboard. Phone users receive the same rent data and dashboard links in a compact comparison table.

## Repository structure

- `index.html` contains the page layout, styling, submarket rent data, dashboard links, and interactions.
- `final_poly.geojson` contains the map polygons and submarket labels.
- `Client logos/` supplies the occupier-logo banner.
- `vendor/maplibre-gl/` contains the locally hosted MapLibre assets.

The map first loads `final_poly.geojson` locally and falls back to the copy hosted on GitHub. The `submarketData` array in `index.html` is the single source for both map popouts and the rents table. It currently reflects Q2 2026 figures from `MASTER COPY Q2 2026 Final.xlsx`.

At phone widths, the map is intentionally replaced by the table. A short notice explains how to open dashboards when the guide is viewed inside LinkedIn, and positively detected LinkedIn in-app browsers intercept dashboard taps with step-by-step instructions instead of sending users to a blocked or blank view.

