# Geospatial Big Data Analysis of Wildfires in Canada

**Technologies:** Python · Apache Spark · PySpark · Spark SQL · GeoPandas · Folium · Machine Learning · Tableau

## Project Overview

This project analyzes historical Canadian wildfire records using Big Data technologies and geospatial analytics. It applies PySpark and Spark SQL to clean, transform, aggregate, and analyze wildfire data, while GeoPandas and Folium support spatial data validation and interactive mapping.

The project investigates temporal wildfire patterns, fire-size distributions, large-fire concentration, reported causes, and differences across reporting agencies. It also incorporates a Random Forest classification approach to predict recorded wildfire cause categories and visualizes the analytical findings through statistical charts, interactive maps, and a Tableau dashboard.

## Project Objectives

1. Collect and prepare historical Canadian wildfire data for Big Data analysis.
2. Use PySpark to clean, transform, and process wildfire records.
3. Analyze the temporal and geographical distribution of recorded wildfires.
4. Examine fire size, reported causes, and burned area across years and reporting agencies.
5. Develop and evaluate a machine-learning classifier for predicting recorded wildfire cause categories.
6. Visualize and interpret wildfire patterns using geospatial maps, statistical charts, and Tableau.

## Dataset

The primary dataset is the **National Fire Database (NFDB)** from Natural Resources Canada.

The project uses a 10,000-record extract containing fields such as:

- Fire identifier
- Year of occurrence
- Fire size in hectares
- Reported cause
- Reporting agency
- Latitude and longitude
- Fire type and other available attributes

The official NFDB point shapefile and summary statistics workbook are used for spatial validation and reference comparisons.

### Data sources

- [NFDB point shapefile and downloads](https://cwfis.cfs.nrcan.gc.ca/downloads/nfdb/fire_pnt/current_version/)
- [NFDB point-data summary statistics workbook](https://cwfis.cfs.nrcan.gc.ca/downloads/nfdb/fire_pnt/current_version/NFDB_point_stats.xlsx)
- [Government of Canada Open Data](https://open.canada.ca/data/en/dataset)

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data processing and analysis |
| Apache Spark / PySpark | Distributed data cleaning, transformation, and aggregation |
| Spark SQL | Structured queries and analytical summaries |
| GeoPandas | Spatial data processing and geometry validation |
| Folium | Interactive wildfire mapping |
| Matplotlib | Statistical visualization |
| scikit-learn | Classification evaluation and confusion matrices |
| PySpark MLlib | Random Forest classification |
| Tableau | Dashboard development and presentation |
| Jupyter Notebook / Google Colab | Development and execution environment |

## Methodology

The project follows a multi-phase analytical workflow:

1. **Data understanding:** Examine dataset structure, fields, distributions, and completeness.
2. **Data cleaning and validation:** Investigate missing values, duplicate identifiers, invalid coordinates, and sentinel geometries while preserving original records.
3. **Big Data aggregation:** Use PySpark and Spark SQL to calculate annual and agency-level fire counts, burned area, and fire-size distributions.
4. **Large-fire concentration analysis:** Calculate the number and proportion of fires exceeding 200 hectares and their contribution to total burned area.
5. **Machine learning:** Develop and evaluate a Random Forest classifier for recorded wildfire cause categories.
6. **Geospatial analysis:** Validate coordinate reference systems and create interactive maps of spatially eligible fire records.
7. **Visualization and reporting:** Present annual trends, cause and agency comparisons, and burned-area comparisons using charts, maps, and Tableau.

## Key Findings

Results from the 10,000-record project extract include:

- **Total records:** 10,000.
- **Total recorded burned area:** approximately 85.43 million hectares.
- **Fires greater than 200 hectares:** 9,865 records, representing 98.65% of the extract.
- **Burned area from fires greater than 200 hectares:** approximately 85.40 million hectares, representing about 99.97% of the extract's recorded burned area.
- **Most represented year by fire count:** 2023, with 965 records.
- **Largest annual recorded burned area:** approximately 17.57 million hectares in 2023.

These findings describe the project extract, not the complete population of Canadian wildfires.

## Geospatial Visualization

The interactive Folium map displays spatially eligible fire locations and provides separate layers for:

- All valid mapped fire records
- Fires exceeding 200 hectares

Marker clustering helps manage overlapping points. Users can zoom in, inspect selected fire attributes, and switch map layers.

## Machine Learning

A Random Forest classifier using PySpark MLlib is developed to predict recorded wildfire cause categories from available fire attributes.

The evaluation workflow includes:

- Training and testing data separation
- Target and feature encoding
- Handling of class imbalance
- Accuracy, precision
