# WorldView

Full-screen country-level world map with CSV-driven journalist intelligence heatmap.

## User View (`index.html`)
- Fullscreen detailed country map.
- Top-right **Admin Access** button (no popup).
- Countries are shaded in retro heatmap colors based on negative-article ratio.
- Hover: shows country summary, journalist counts, and article metrics.
- Click: shows journalists, biases, photos, and expandable owner details.

## Admin View (`admin.html`)
- Requires login.
- Upload CSV and map data is saved locally for rendering in the map.

### Demo Admin Login
- `admin` / `worldview2026`

## CSV columns
`country,journalists_count,zero_percent_club,articles,negative_articles,journalist_name,journalist_photo,biases,owner_name,owner_photo,owner_organization`

## Run
```bash
python3 -m http.server 8000
```
Open `http://localhost:8000/index.html`.
