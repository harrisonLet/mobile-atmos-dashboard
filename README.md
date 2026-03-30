# Mobile Atmos Dashboard

A web-based mobile atmospheric data dashboard for visualizing and analyzing field campaign measurements in near real time. Built for researchers, students, and the interested public to explore multi-species trace gas and meteorological data collected from mobile platforms.

Built and maintained by **Harrison LeTourneau**, University of Utah — Land-Atmosphere Interactions Research Group.

---

## Overview

The dashboard is organized around field campaigns and provides two core interfaces:

- **Viewer** — An interactive map viewer displaying GPS-tracked measurement routes using pre-generated Leaflet maps, organized by campaign and date.
- **Analysis** — An interactive plotting interface powered by Plotly, allowing users to explore time series, vertical profiles, and multi-species comparisons for each measurement day.

Data is organized by campaign (e.g., `slv`, `usos`) and date, with each day containing a CSV of measurements and a corresponding map HTML file.

---

## Project Structure

```
dashboard/
├── index.html              # Landing page
├── about/
│   └── index.html          # About the project and team
├── viewer/
│   └── index.html          # Leaflet map viewer
├── analysis/
│   └── index.html          # Plotly interactive analysis plots
└── data/
    └── slv/                # Salt Lake Valley campaign data
        └── YYYYMMDD/
            ├── YYYYMMDD.csv
            └── YYYYMMDD_map.html
```

---

## Campaigns

| Campaign ID | Description |
|-------------|-------------|
| `slv`       | Salt Lake Valley campaign (Winter 2026) |
| `arc`       | Utah Summer Ozone Study (USOS) (Summer 2026) from the Air Resources Car (ARC) |

---

## Usage

The dashboard is hosted on a server and is static. The original Mobile Atmos Dashboard is currently hosted at home.chpc.utah.edu/~u1460207/dashboard/.

### Viewer

1. Select a campaign from the home page or navigation menu.
2. Choose a date to load the pre-generated GPS-tracked Leaflet map for that day.
3. The map displays the measurement route with spatial context.

### Analysis

1. Select a campaign and date.
2. The analysis page loads interactive Plotly charts for that day's data.
3. Use the Plotly toolbar to zoom, pan, and scale.
4. Use the select tool to drag horizontally across a range of data. All plots will update based on the range of selected data.

---

<!-- ## Data

For your own use, or to request that data might be added to the dashboard hosted at home.chpc.utah.edu/~u1460207/dashboard/, see [DATA_FORMAT.md](DATA_FORMAT.md) for a full description of the CSV data schema. -->

---

## Related Projects

- **mobilelab** — Python-based data ingestion and analysis toolkit. Used to generate the files consumed by this dashboard.

---

## Citation

If you use this dashboard or the data it presents in your work, please cite:

> LeTourneau, H. (2025). *Mobile Atmos Dashboard*. University of Utah, Land-Atmosphere Interactions Research Group.

---

## Contact

**Harrison LeTourneau**  
Land-Atmosphere Interactions Research Group  
University of Utah  
harrison.letourneau@gmail.com

For bug reports or feature requests, please open an issue on this repository or email me directly.

---