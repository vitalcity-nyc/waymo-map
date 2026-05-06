# Waymo in America — interactive map

A simple, embeddable U.S. map showing where Waymo operates robotaxi service, where it has announced 2026 launches, where it has tested without commercial deployment, and how state law treats driverless commercial operation.

**Live:** https://vitalcity-nyc.github.io/waymo-map/
**Methodology:** [methodology.md](methodology.md)

## Embed in a Vital City story

Paste this into a Ghost HTML card. The `?mode=compact` parameter strips the title block and shrinks the map for inline use.

```html
<iframe src="https://vitalcity-nyc.github.io/waymo-map/?mode=compact"
        loading="lazy"
        style="width:100%; height:640px; border:0;"
        title="Waymo robotaxi service map">
</iframe>
```

For a full-width standalone version with title, stats, and footer, drop the `?mode=compact`:

```html
<iframe src="https://vitalcity-nyc.github.io/waymo-map/"
        loading="lazy"
        style="width:100%; height:780px; border:0;"
        title="Waymo robotaxi service map">
</iframe>
```

## Files

- `index.html` — the map (single self-contained file: Leaflet, scoped CSS, inline data)
- `methodology.md` — every data point, source, and assumption
- `README.md` — this file

## Updating the data

Edit the `cities` array and `stateClass` map at the top of the script block in `index.html`, update the "Last updated" stamp in the footer and methodology, and push to `main`. GitHub Pages will redeploy automatically.

## Built with

- [Leaflet](https://leafletjs.com/) 1.9.4
- CARTO Positron basemap
- U.S. state boundaries from the [PublicaMundi MappingAPI](https://github.com/PublicaMundi/MappingAPI) GeoJSON
- Vital City color tokens and typography
