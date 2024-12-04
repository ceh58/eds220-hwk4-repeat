# Visualizing the impact of the Thomas Fire (2017)
Author: Carmen Hoyt

This repository hosts the notebooks and data needed to conduct and analysis of the Thomas Fire (2017) in Santa Barbara and Ventura Counties, California. Using false color imagery, we can visualize the impact (the burn scar) of the Thomas Fire. Air Quality Index (AQI) data helps us to visualize additional environmental impacts of the fire. 

## Data

Three datasets are used in this analysis:

1. Landsat Data:
   
A cleaned, simplified collection of bands (red, green, blue, nir, swir) from Landsat Collection 2 Level-2 (collected by Landsat 8 satellite).

Microsoft Open Source, Matt McFarland, Rob Emanuele, Dan Morris, & Tom Augspurger. (2022). microsoft/PlanetaryComputer: October 2022 (2022.10.28). Zenodo. https://doi.org/10.5281/zenodo.7261897
Accessed: November 19, 2024

2. Fire Perimeter Data:
   
Open-source data containing information from the spatial distribution of past fires in California published by the State of California (and downloaded as a shapefile). 

State of California, Kimberly Wallin. (2024). CAL FIRE: May 2024 (2024.05.14). https://catalog.data.gov/dataset/california-fire-perimeters-all-b3436
Accessed: November 19, 2024

3. Air Quality Index (AQI) Data:

This analysis directly imports the US AQI (by county) data for [2017](https://aqs.epa.gov/aqsweb/airdata/daily_aqi_by_county_2017.zip) and [2018](https://aqs.epa.gov/aqsweb/airdata/daily_aqi_by_county_2018.zip) via zip file. Both datasets will need to be filtered for Santa Barbara County.

U.S. Environmental Protection Agency. (2024). Air Quality Index Daily Values Report: July 2024 (2024.07.23). [https://www.epa.gov/outdoor-air-quality-data/air-quality-index-daily-values-report](https://www.epa.gov/outdoor-air-quality-data/air-quality-index-daily-values-report)
Accessed: October 22, 2024

## Repository Structure
```
├── data
│  ├── thomas_fire.cpg
│  ├── thoams_fire.dbf
│  ├── thomas_fire.prj
│  ├── thomas_fire.shp
│  └── thomas_fire.shx
├── .gitignore
├── README.md
├── aqi-analysis.ipynb
├── false-color-analysis.ipynb
└── fire-perimeter.ipynb
```

The fire-perimeter.ipynb notebook details the steps to isolate the boundary of the Thomas Fire in 2017 from the full "Fire Perimeter" dataset by filtering the geo-dataframe downloaded from the State of California. The data folder houses the resulting shapefile `thomas_fire.shp`.

The false-color-analysis.ipynb notebook uses false color imagery to visualize the impact (the burn scar) of the Thomas Fire in 2017 by assigning infrared bands to visible colors and plotting shapefiles over the resulting images. Necessary steps include cleaning rasters and matching Coordinate Reference Systems (CRSs).  

The aqi-analysis.ipynb notebook outlines the steps necessary to obtain an AQI graph for Santa Barbara County for 2017-2018.

## Acknowledgments

Thank you to Professor Carmen Galaz-García (@carmengg on GitHub) for preparing the Landsat data and assigning these homework assignments for EDS 220.
