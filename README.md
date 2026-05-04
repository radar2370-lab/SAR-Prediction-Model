# SAR Probability Ring Simulator

An interactive web-based Search and Rescue (SAR) probability ring simulator developed by Nick Radom in an Independent Study on Search and Rescue.

## About

This tool generates spatial probability rings for missing persons SAR operations based on statistical data from the International Search and Rescue Incident Database (ISRID). Users can input any location, subject type, terrain, and hours missing to instantly generate evidence-based search zones that can be exported directly into CalTopo for field use.

## Features

- Interactive map powered by Leaflet.js and OpenStreetMap — no API key required
- Address or lat/long search to place the Last Known Point (LKP) anywhere
- Five subject categories based on ISRID behavioral profiles:
  - Dementia patient
  - Hiker
  - Lost child (6–12)
  - Despondent adult
  - Mental illness
- Terrain adjustment multipliers for mountain, forest, urban, and flat environments
- Time elapsed adjustment — rings expand as hours missing increases
- Four probability rings at 25%, 50%, 75%, and 95% based on ISRID statistics
- Street, topographic, and satellite basemap options
- Export to KML for direct import into CalTopo
- Export to GPX for Garmin devices and other field navigation tools

## Data Sources

Probability ring distances are derived from:

- **Koester, R.J. (2008).** Lost Person Behavior: A Search and Rescue Guide on Where to Look for Land, Air and Water. dbS Productions. — The foundational reference text for SAR lost person behavior statistics
- **ISRID — International Search and Rescue Incident Database** — 150,000+ SAR incidents collected globally by Dr. Robert Koester

Terrain multipliers applied to base ISRID distances:

| Terrain | Multiplier | Rationale |
|---------|-----------|-----------|
| Mountain / Appalachian | 0.70 | Steep slopes reduce travel distance ~30% |
| Dense forest | 0.80 | Navigation difficulty reduces distance ~20% |
| Urban / Suburban | 1.20 | Road networks increase distance ~20% |
| Flat / Rural | 1.10 | Open terrain increases distance ~10% |

## How to Use

1. Enter an address, place name, or lat/long coordinates in the LKP search box and click **Set LKP** — or click anywhere on the map directly
2. Select your subject type, terrain, and hours missing
3. Probability rings generate automatically on the map
4. Review ring distances and expected subject behaviors
5. Click **Download KML for CalTopo** to export your rings
6. In CalTopo: Add → Import File → upload the KML file

## How to Import into CalTopo

1. Click **Download KML for CalTopo** in the simulator
2. Open [CalTopo](https://caltopo.com)
3. Click **Add → Import File**
4. Upload the downloaded `.kml` file
5. Your LKP marker and all four probability rings will appear on your CalTopo map

## Technology

- [Leaflet.js](https://leafletjs.com) — Open source interactive mapping library
- [OpenStreetMap](https://www.openstreetmap.org) — Free open geographic data
- [Nominatim](https://nominatim.org) — Free OpenStreetMap geocoding API for address search
- [Esri World Imagery](https://www.esri.com) — Satellite basemap layer
- [OpenTopoMap](https://opentopomap.org) — Topographic basemap layer
- Plain HTML, CSS, and JavaScript — no frameworks, no dependencies beyond Leaflet

## Academic Context

This simulator was developed as part of an independent study project examining how GIS mapping tools can improve search and rescue operations for missing persons through spatial probability analysis. The project was completed for the Emergency & Disaster Management program at Western Carolina University (2026).

The interactive simulator was developed with AI-assisted coding using Claude (Anthropic, 2026), incorporating ISRID statistical data and custom terrain multipliers designed for this research. The research question, methodology, data selection, and analytical framework were developed by the student researcher.

## References

- Koester, R.J. (2008). *Lost Person Behavior: A Search and Rescue Guide on Where to Look for Land, Air and Water.* dbS Productions.
- National Missing and Unidentified Persons System (NamUs). (2024). Reports and Statistics. National Institute of Justice. https://namus.nij.ojp.gov
- Sava, E., Twardy, C., Koester, R., & Sonwalkar, M. (2016). Evaluating Lost Person Behavior Models. *Transactions in GIS, 20*(1), 38–53.
- Esri. (2012). Modeling the Movement of Lost People. *ArcNews*, Fall 2012.
- U.S. Geological Survey. (2024). The National Map. https://apps.nationalmap.gov

## License

This project is open source and free to use for educational and non-commercial SAR planning purposes. If you use this tool operationally, always verify probability distances against current ISRID data for your region and subject category.
