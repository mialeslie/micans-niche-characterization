# Amastra micans Niche Characterization

## Overview
This repository contains R code for characterizing the ecological niche of *Amastra micans*, a Hawaiian land snail species. The code integrates various environmental datasets, such as climatic variables and soil data, with snail occurrence records and exclosures data. It uses geospatial analysis tools and environmental modeling techniques to generate visual and statistical outputs.

### Key Features
- Import of snail occurrence data and environmental variables (e.g., climate, soil, vegetation, elevation).
- Conversion of occurrence points to spatial objects for geospatial analysis.
- Extraction of environmental variables at snail occurrence and exclosure sites.
- Niche modeling using climatic and environmental variables to generate histograms, 2D plots, and 3D plots.
- Ranking of exclosure sites based on niche suitability.
- Automated generation of plots and data exports for further analysis.

## Requirements
The following R packages are required for the analysis:

- `hypervolume`
- `sf`
- `terra`
- `raster`
- `RColorBrewer`
- `dplyr`
- `ggplot2`
- `cowplot`
- `plotly`
- `htmlwidgets`
- `tools`

To install all necessary packages, run:

```r
install.packages(c("hypervolume", "sf", "terra", "raster", "RColorBrewer", "dplyr", "ggplot2", "cowplot", "plotly", "htmlwidgets", "tools"))
```

## Data Structure

The project is organized as follows:

```
Data/
├── Snail_data/
│   ├── micans.csv
│   └── oahu_exclosures.csv
├── Environmental_data/
│   ├── Elevation/
│   │   └── Tif/
│   ├── Actual Evapotranspiration/
│   ├── Available Soil Moisture/
│   └── ...
└── HI_shapefile/
```
-   **Snail Data:** CSV files containing occurrence records of *Amastra micans*.

-   **Environmental Data:** Includes raster files for climatic variables (e.g., temperature, precipitation) and shapefiles for environmental features (e.g., soil types, vegetation).

## Usage

To run the analysis and generate the outputs, open the R Markdown file and knit it to the specified output format. The code will automatically load the required data, perform geospatial operations, and generate output plots.

The outputs include:

-   1D histograms of environmental variables at snail locations and exclosure sites.

-   2D scatter plots of paired environmental variables.

-   Interactive 3D plots visualizing multiple environmental dimensions.

## Outputs

Generated outputs are stored in the `Outputs/` directory:

-   **Env_output_plots/**: Environmental variable plots for each selected island.

-   **1D_plots/**: Histograms showing the distribution of environmental variables.

-   **2D_plots/**: Scatter plots of environmental variables.

-   **3D_plots/**: HTML files for interactive 3D plots.

-   **exclosure_rankings.csv**: A CSV file ranking the exclosure sites based on environmental suitability for *Amastra micans*.

## Customization

To analyze a different island or exclosure site, adjust the `chosen_island` variable in the script. The available options include:

-   `"bigisland"`

-   `"lanai"`

-   `"maui"`

-   `"molokai"`

-   `"kauai"`

-   `"oahu"`

-   `"waianae"`

-   `"koolau"`

The code will automatically update the analysis and plots based on the chosen island or mountain range.

## Contributions

Contributions and suggestions for improvements are welcome. Please fork the repository and submit a pull request with your changes.

## Authors

-   Chandra Earl

-   Mia Leslie
