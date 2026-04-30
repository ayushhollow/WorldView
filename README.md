# WorldView

Full-screen country-level world map with CSV-driven journalist intelligence heatmap.

## User View (`index.html`)
- Fullscreen detailed country map.
- Top-right **Admin Access** button (no popup).
- Countries are shaded in retro heatmap colors based on negative-article ratio.
- Hover: shows country summary, journalist counts, and article metrics.
- Click: shows journalists, biases, photos, and expandable owner details.
- Map wraparound is disabled at global zoomed-out level (single world only).

## Admin View (`admin.html`)
- Requires login.
- Upload CSV and map data is saved locally for rendering in the map.
- Supports both header formats:
  - `country,journalists_count,zero_percent_club,articles,negative_articles,...`
  - `countries,Count,Zero% Club,Articles/Negative,...`

### Demo Admin Login
- `admin` / `worldview2026`

## CSV columns
`country,journalists_count,zero_percent_club,articles,negative_articles,journalist_name,journalist_photo,biases,owner_name,owner_photo,owner_organization`

## Run
```bash
python3 -m http.server 8000
```
Open `http://localhost:8000/index.html`.
A full-screen world viewer with country-level hover details and protected special tools.

## Main experience
- Full-screen interactive world map.
- Hover over **each country** to get country-level information in a top overlay panel.
- Click a country to open a pinned popup with details.

## Special access tool (login required)
- A protected text-to-table utility is available only after login.
- Converts mixed-format text into table rows.
- Supports sorting and CSV export.

## Demo login
- Username: `admin`
- Password: `worldview2026`

## Run locally
```bash
python3 -m http.server 8000
```
Open `http://localhost:8000`.
