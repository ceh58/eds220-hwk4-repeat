# Visualizing the impact of the Thomas Fire (2017)
Author: Carmen Hoyt

## Data

Two datasets were used in this analysis:

1. Landsat Data:
   
A cleaned, simplified collection of bands (red, green, blue, nir, swir) from Landsat Collection 2 Level-2 (collected by Landsat 8 satellite).

Microsoft Open Source, Matt McFarland, Rob Emanuele, Dan Morris, & Tom Augspurger. (2022). microsoft/PlanetaryComputer: October 2022 (2022.10.28). Zenodo. https://doi.org/10.5281/zenodo.7261897
Accessed: November 19, 2024

2. Fire Perimeter Data:
   
Open-source data containing information from the spatial distribution of past fires in California published by the State of California (and downloaded as a shapefile). 

State of California, Kimberly Wallin. (2024). CAL FIRE: May 2024 (2024.05.14). https://catalog.data.gov/dataset/california-fire-perimeters-all-b3436
Accessed: November 19, 2024

## Repository Structure
```
├── LICENSE
├── .gitignore
├── README.md
├── hwk4-task2-fire-perimeter-HOYT.ipynb
└── hwk4-task2-false-color-HOYT.ipynb
```

The hwk4-task2-fire-perimeter-HOYT.ipynb notebook isolates the boundary of the Thomas Fire in 2017 from the Fire Perimeter dataset by filtering the geo-dataframe downloaded from the State of California.

The hwk4-task2-false-color-HOYT.ipynb notebook uses false color imagery to visualize the impact (the burn scar) of the Thomas Fire in 2017 by assigning infrared bands to visible colors and plotting shapefiles over the resulting images. Necessary steps include cleaning rasters and matching Coordinate Reference Systems (CRSs).  

All data was stored locally in a "data" folder but not pushed to GitHub due to its large size.

## Acknowledgments

Thank you to Professor Carmen Galaz-García (@carmengg on GitHub) for preparing the Landsat data and assigning this homework.
