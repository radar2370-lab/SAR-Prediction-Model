# SAR Probability Ring Simulator v1.2.0

> ⚠️ **Beta software — not intended for official or operational use.** This tool uses historical ISRID data and should only be used as a planning aid. Always defer to your team's protocols and qualified personnel.

A browser-based Search and Rescue planning tool that generates ISRID-based probability rings around a Last Known Point (LKP) and exports them directly to CalTopo via KML or GPX.

Built by a SAR volunteer for SAR volunteers.

---

## Features

- **15 ISRID subject categories** — including Dementia/Alzheimer's, Autism spectrum, Lost child/Teen (auto-selected by age), Hiker, Hunter, Climber, Skier, ATV rider, Equestrian, Despondent adult, and more
- **Age-aware child profiling** — selecting "Lost child / Teen" automatically applies the correct ISRID data profile based on the subject's age
- **Terrain adjustment** — ring distances are automatically scaled for Mountain/Appalachian, Dense forest, Urban/Suburban, and Flat/Rural terrain
- **Time adjustment** — ring distances scale with hours missing
- **Interactive map** — click anywhere on the map to set or move the LKP; supports Street, Topographic, and Satellite basemaps
- **Autocomplete address search** — type any address or place name and suggestions appear instantly, powered by OpenStreetMap
- **Export to CalTopo** — download a KML file with all four probability rings and the LKP marker, ready to import into CalTopo in seconds
- **GPX export** — for use with other mapping tools
- **Expected behavior panel** — ISRID-based behavioral notes for each subject type to guide search strategy

---

## Probability Rings

Each ring represents a cumulative probability boundary based on ISRID data (Koester, 2008):

| Ring | Probability | Description |
|------|-------------|-------------|
| Ring 1 | 25% | 25% of subjects found within this radius |
| Ring 2 | 50% | 50% of subjects found within this radius |
| Ring 3 | 75% | 75% of subjects found within this radius |
| Ring 4 | 95% | 95% of subjects found within this radius (outer boundary) |

---

## How to Use

1. **Set the LKP** — type an address in the search box or click directly on the map
2. **Enter subject parameters** — select subject type, enter age, choose terrain, and enter hours missing
3. **Review the rings** — the map updates automatically with color-coded probability rings
4. **Export** — click **Download KML for CalTopo** and import the file into CalTopo via *Add → Import File*

---

## Importing into CalTopo

1. Download the KML file from the Export section
2. Open your CalTopo map
3. Click **Add → Import File**
4. Upload the KML file
5. Your LKP and all four probability rings will appear instantly

---

## Data Source

All probability ring distances are derived from the **International Search and Rescue Incident Database (ISRID)**, as published in:

> Koester, R.J. (2008). *Lost Person Behavior*. dbS Productions.

ISRID contains data from over 150,000 search and rescue incidents worldwide and is the industry standard reference for lost person behavior statistics.

---

## Tech Stack

- Plain HTML, CSS, and JavaScript — no frameworks, no dependencies to install
- [Leaflet.js](https://leafletjs.com/) for the interactive map
- [OpenStreetMap Nominatim](https://nominatim.org/) for address search
- Hosted via GitHub Pages

---

## Disclaimer

This tool is in active development and is provided as-is. It is **not a substitute for professional SAR training, ICS protocols, or qualified incident command decisions.** Ring distances are statistical estimates based on historical data and may not reflect conditions of any specific incident.
