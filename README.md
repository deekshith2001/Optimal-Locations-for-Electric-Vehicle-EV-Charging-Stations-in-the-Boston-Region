Author: Deekshith Komira
Course: UEP 232 - Introduction to GIS
Semester: Fall 2023
Submission Date: 12/18/2023

Project Description
This project identifies optimal locations for EV charging stations in the Boston region using GIS-based multi-criteria suitability analysis. It considers various factors, including EV ownership, socioeconomic indicators, and existing infrastructure, to provide actionable insights for promoting EV adoption and reducing GHG emissions.

Repository Structure
kotlin
Copy
Edit
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
Methodology
Data Collection:

Used datasets from MassGIS, the American Community Survey, and the Alternative Fuels Data Center.
Data spanned 2009–2014 and included census block groups, land use classifications, elevation, and existing EV station locations.
Data Processing:

Converted polygon features to raster datasets.
Calculated proximity using Euclidean distance.
Generated slope rasters from elevation data.
Weighted Overlay Analysis:

Criteria such as land use, median income, population density, and incline were assigned weights.
Generated a suitability map highlighting optimal EV station locations.
Visualization:

Created maps to present results, emphasizing high-suitability regions.
Results
The weighted overlay analysis identified areas with high suitability for EV charging stations, including:

Eastern sectors like Waltham and Newton.
Southeast areas such as Franklin and Foxborough.
Neighborhoods near Boston, such as Roxbury, Somerville, and Chelsea.
Data Sources
Dataset	Description	Source
Census Block Groups	Base for neighborhood delineation	MassGIS
EV Ownership Statistics	Block groups with at least one EV owner	MAPC
American Community Survey	Data on population density, income, and commute distances	Census
Alternative Fuels Data Center	Current EV charging station locations	AFDC
Land Use	Land use classifications	MassGIS
Elevation Model	Topographic information	MassGIS
Vehicle Statistics	Clustered residents with or without EV ownership	MOR-EV
References
Smith, J. A., et al. (2020). A GIS-Based Approach for Optimal Siting of Electric Vehicle Charging Stations in Urban Areas.
Zhang, Y., & Iman, K. (2018). A Multi-Factor GIS Method for Identifying Optimal EV Charging Station Locations.
Additional references in references/citation_list.md
