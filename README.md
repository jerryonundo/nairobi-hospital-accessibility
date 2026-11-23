# Spatial Assessment of Hospital Accessibility in Nairobi County, Kenya

![GIS](https://img.shields.io/badge/Domain-GIS%20%7C%20Spatial%20Analysis-blue)
![Software](https://img.shields.io/badge/Software-QGIS-green)
![Analysis](https://img.shields.io/badge/Analysis-Network%20Accessibility-orange)

## Project Overview

This project investigates the spatial accessibility of hospitals across Nairobi County, Kenya, using Geographic Information Systems (GIS), road-network analysis and population distribution data.

The assessment uses hospital locations, the OpenStreetMap road network and WorldPop 2025 population estimates to examine the population within different network-distance thresholds and identify areas beyond a 5 km hospital service area.

The project demonstrates how spatial analysis can support healthcare accessibility assessment, evidence-based planning and identification of underserved communities.

## Study Area

**Nairobi County, Kenya**

The analysis covers the county's administrative area and incorporates ward-level assessment.

## Objectives

- Assess hospital accessibility using road-network distance.
- Delineate cumulative service areas at 1 km intervals up to 5 km.
- Estimate the population within hospital service areas.
- Identify areas and wards with populations outside the 5 km service-area threshold.
- Present the spatial distribution of underserved populations through thematic maps.

## Data Sources

| Dataset | Source |
|---|---|
| Hospital locations | OpenStreetMap |
| Road network | OpenStreetMap / Geofabrik |
| Population estimates | WorldPop 2025 |
| County boundary | GADM |
| Ward boundaries | Humanitarian Data Exchange (HDX) |

Original data sources and their licensing conditions should be consulted before redistribution.

## Methodology

The project was undertaken using QGIS and the QNEAT3 network analysis plugin.

The main analytical stages included:

1. Data acquisition and preparation.
2. Coordinate reference system harmonisation using EPSG:32737.
3. Road-network preparation and hospital point connectivity checks.
4. Network-based service-area analysis.
5. Dissolution of overlapping service areas by distance threshold.
6. Population estimation using raster zonal statistics.
7. Identification of areas outside the 5 km service-area threshold.
8. Ward-level underserved population assessment.
9. Cartographic visualisation and interpretation.

## Key Findings

The unique dissolved 5 km service-area analysis estimated that approximately **5.36 million people (92.22%)** were within the mapped service areas.

The corrected unserved-area analysis estimated approximately **441,926 people** outside the 5 km service-area threshold.

These two estimates did not reconcile completely. The difference is documented as an analytical limitation and should be considered when interpreting the results.

## Map Outputs


## Map Outputs

### Map 1: Spatial Distribution of Health Facilities in Nairobi County

![Spatial Distribution of Health Facilities](<maps/Spatial Distribution of Health Facilities in Nairobi County.png>)

### Map 2: Ward-Level Healthcare Accessibility Gaps

![Ward-Level Healthcare Accessibility Gaps](<maps/Ward-Level Healthcare Accessibility Gaps..png>)

### Map 3: Distribution of Underserved Population by Ward

![Distribution of Underserved Population](<maps/Distribution of Underserved Population by Ward.png>)

## Software and Tools

- QGIS
- QNEAT3
- GDAL
- OpenStreetMap
- WorldPop

## Limitations

- Differences in the positional alignment of GADM county boundaries and HDX ward boundaries.
- OpenStreetMap road and healthcare facility data may be incomplete or vary in positional accuracy.
- Network distance does not represent actual travel time.
- Hospital capacity, staffing and service availability were not incorporated.
- Population estimates depend on the accuracy and resolution of the WorldPop raster.
- A residual difference remains between the independently calculated covered and unserved population estimates.
- The assessment was not field-validated.

## Repository Structure

```text
nairobi-hospital-accessibility/
├── README.md
├── maps/
├── images/
├── reports/
├── qgis/
├── analysis/
└── data/
```

## Conclusion

This project demonstrates the application of GIS-based network analysis and population distribution data to assess geographical patterns of hospital accessibility in Nairobi County.

It provides a spatial evidence base for understanding potential accessibility gaps and highlights considerations for future healthcare accessibility assessments.

---

**Project:** Spatial Assessment of Hospital Accessibility in Nairobi County, Kenya  
**Tools:** QGIS, QNEAT3 and GDAL  
**Coordinate Reference System:** EPSG:32737
