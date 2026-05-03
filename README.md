# Urban Heat Zürich West

Long-term analysis of Land Surface Temperature (LST) and vegetation 
cover (NDVI) across Zürich West (Kreise 3, 4, 5, 9, 10) from 1985–2024 
using Landsat satellite imagery.

## Research Question
Has Land Surface Temperature in Zürich West increased measurably between 
1985 and 2024, and do Quartiere with declining vegetation show 
systematically higher warming rates?

## Data Sources
- Landsat LST/NDVI time series: [Google Drive](https://drive.google.com/drive/folders/1SmEzlCAJJGYY-TdB58JX6ADvVxSQrMqj)
- Quartier-Shapefiles: [Stadt Zürich Open Data](https://www.stadt-zuerich.ch/geodaten/download/Gebietseinteilung_GSZ___GB_Park__und_Gruenanlagen?format=10005)

## Setup
1. Clone this repository
2. Download raw data from Google Drive and place in `data/raw/`
3. Download Quartier-Shapefiles and place in `data/vector/`
4. Create the conda environment: `conda env create -f environment.yml`
5. Activate it: `conda activate urban-heat`

## Execution Order
Run notebooks in this order:
1. `notebooks/01_data_inspection.ipynb`: Inspect rasters, check cloud cover
2. `notebooks/02_preprocessing.ipynb`: Masking, clipping to Zurich West
3. `notebooks/03_analysis.ipynb`: Zonal stats, trends, correlation
4. `notebooks/04_visualisation.ipynb`: All plots and maps