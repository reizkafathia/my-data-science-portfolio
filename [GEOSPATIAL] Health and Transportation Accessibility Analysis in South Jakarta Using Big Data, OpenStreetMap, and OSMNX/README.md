# Health and Transportation Accessibility in South Jakarta Using OpenStreetMap and OSMNX

## Introduction

This project was developed for the *Analisis Data Tidak Terstruktur* final exam at Universitas Indonesia. The objective is to analyze the accessibility of healthcare and transportation in South Jakarta by leveraging geospatial data from OpenStreetMap (OSM) and performing spatial network analysis using the OSMNX Python library.

## Motivation

South Jakarta is a dense urban area where equal access to healthcare is critical but often unevenly distributed. This analysis seeks to explore disparities in healthcare accessibility and road network connectivity, with the ultimate goal of supporting better urban planning and resource allocation.

## Data

- **Street Network & Hospital Locations**: Extracted using OSMNX from OpenStreetMap.
- **Population Data**: Official data from BPS Jakarta Selatan (2024), includes total population by sub-district (kecamatan).
- **Study Area**: 11 sub-districts in South Jakarta, DKI Jakarta, Indonesia.

## Methodology

1. **Data Collection**
   - Extracted street network and hospital locations using OSMNX.
   - Collected population data by kecamatan from BPS.

2. **Network Analysis**
   - Computed street network stats (nodes, edges, connectivity).
   - Calculated centrality (degree centrality) to identify strategic intersections.

3. **Accessibility Analysis**
   - Merged population data with hospital distribution.
   - Calculated population-per-hospital ratios as a measure of healthcare access.

4. **Visualization**
   - Mapped hospital locations and road networks.
   - Created interactive maps using Folium.
   - Plotted ratios and population distributions by district.

## Results

- **Street Network**: 24,277 nodes and 53,632 road segments.
- **Hospitals**: 97 facilities unevenly distributed across districts.
- **Population**: 4,759,366 residents across 11 districts.
- **Accessibility Gaps**:
  - **Best**: Setiabudi (14,632 residents per hospital)
  - **Worst**: Kota Jakarta Selatan (297,460 residents per hospital)
- **Distance to Hospitals**: Average distance to the nearest hospital is ~0.73 km.

## Insights and Recommendations

- Significant disparities in healthcare accessibility exist between districts.
- Some high-density areas have few or no nearby hospitals.
- Recommendations:
  - Add more hospitals in underserved districts (e.g., Kota Jakarta Selatan).
  - Redistribute healthcare facilities more evenly.
  - Consider hospital capacity and service type in future analysis.

## Conclusion

This project successfully integrates geospatial and socio-economic data to assess healthcare accessibility in South Jakarta. The insights and visualizations can support government or city planners in making more equitable infrastructure decisions.

