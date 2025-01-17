# Optimal Locations for Electric Vehicle (EV) Charging Stations in the Boston Region

## Overview
This project identifies optimal locations for EV charging stations within the Boston region by leveraging GIS-based multi-criteria suitability analysis. The analysis incorporates various factors, including EV ownership, socioeconomic indicators, commuting patterns, and existing infrastructure, to support the growth of EV adoption and reduction of greenhouse gas (GHG) emissions from the transportation sector.

---

## Project Details

**Course**: UEP 232 - Introduction to GIS  
**Semester**: Fall 2023  
**Author**: Deekshith Komira  
**Submission Date**: December 18, 2023

---

## Methodology

### 1. Data Collection
The following data sources were used:

- **MassGIS Data**: Census block groups, land use classifications, and elevation models.
- **Massachusetts Vehicle Summary Statistics (2009-2014)**: EV ownership data by block groups.
- **American Community Survey (ACS)**: Population density, income, and commute distances.
- **Alternative Fuels Data Center (AFDC)**: Locations of existing EV charging stations.

### 2. Data Processing
- Converted polygon features to raster datasets using the Feature-to-Raster tool.
- Determined proximity to existing charging stations using Euclidean distance calculations.
- Generated slope rasters from elevation data and clipped all input layers to the Boston region boundary.

### 3. Weighted Overlay Analysis
- Reclassified and assigned scores (1-10) to each factor based on suitability.
- Weighted factors based on their influence on EV station suitability:
  - **Land use classification**: 25%
  - **Median income**: 20%
  - **Proximity to charging stations**: 15%
  - **Median commuting distance**: 15%
  - **EV ownership**: 10%
  - **Population density**: 10%
  - **Slope**: 5%
- Combined weighted factors to create a final suitability map.

### 4. Visualization
Generated maps highlighting regions with high suitability for EV charging station deployment, including areas in Waltham, Newton, Franklin, Foxborough, Roxbury, Somerville, and Chelsea.

---

## Results
The analysis produced a suitability map showcasing areas ideal for future EV charging stations. The selected locations balance accessibility, socioeconomic factors, and existing infrastructure to optimize EV usage.

---

## Repository Structure
```
├── data/
│   ├── census_block_groups.geojson
│   ├── ev_ownership.csv
│   ├── ev_charging_stations.geojson
│   ├── land_use.shp
│   ├── elevation_model.tif
│   └── commute_distances.csv
├── scripts/
│   ├── data_preprocessing.py
│   ├── weighted_overlay_analysis.py
│   ├── map_visualization.py
│   └── slope_calculation.py
├── results/
│   ├── final_suitability_map.png
│   └── report.pdf
├── references/
│   └── citation_list.md
├── README.md
└── LICENSE
```

---

## Data Sources
| **Dataset**                     | **Description**                                              | **Source**                                                                 |
|----------------------------------|--------------------------------------------------------------|-----------------------------------------------------------------------------|
| Census Block Groups              | Neighborhood delineation.                                    | [MassGIS](https://www.mass.gov/orgs/massgis-bureau-of-geographic-information) |
| EV Ownership Statistics          | Block groups with at least one EV owner.                    | [MAPC](https://www.mapc.org/learn/data/)                                   |
| American Community Survey        | Population density, income, commute distances.              | [Census](https://www.census.gov/programs-surveys/acs)                      |
| Alternative Fuels Data Center    | Existing EV charging station locations.                     | [AFDC](https://afdc.energy.gov/fuels/electricity_stations.html)            |
| Land Use                         | Land use classifications.                                   | [MassGIS](https://www.mass.gov/info-details/massgis-data-2016-land-coverland-use) |
| Elevation Model                  | Topographic information.                                    | [MassGIS](https://www.mass.gov/info-details/massgis-data-lidar-dem-and-shaded-relief) |

---

## References
1. Smith, J. A., et al. (2020). *A GIS-Based Approach for Optimal Siting of Electric Vehicle Charging Stations in Urban Areas*. Transportation Research Part D. [DOI:10.1016/j.trd.2020.102451](https://doi.org/10.1016/j.trd.2020.102451)
2. Zhang, Y., & Iman, K. (2018). *A Multi-Factor GIS Method for Identifying Optimal EV Charging Station Locations*. ICA Proceedings. [DOI:10.5194/ica-proc-1-127-2018](https://doi.org/10.5194/ica-proc-1-127-2018)
3. Erbas, M., et al. (2018). *Optimal Siting of EV Charging Stations: A GIS-Based Multi-Criteria Decision Analysis*. Energy. [DOI:10.1016/j.energy.2018.08.140](https://doi.org/10.1016/j.energy.2018.08.140)
4. Berman, M., et al. (2019). *Optimal Sizing and Siting of EV Charging Stations*. IEEE Symposium on Computers and Communications. [DOI:10.1109/ISCC47284.2019.8969689](https://doi.org/10.1109/ISCC47284.2019.8969689)
5. Sanchez, H., et al. (2019). *Optimal Sizing and Locations of EV Charging Stations Including Multiple Scenarios*. IET Smart Grid. [DOI:10.1049/iet-stg.2019.0363](https://doi.org/10.1049/iet-stg.2019.0363)

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
