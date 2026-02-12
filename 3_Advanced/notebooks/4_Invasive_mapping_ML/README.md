# Using Cloud-Native Tools to Map Invasive Species with Supervised Machine Learning

![invasive mapping](img/pines.jpg)
*Image credit: Daniel Case*

In this notebook, you will use cloud-native geospatial tools and machine learning to map invasive species using Sentinel-2 satellite imagery. You will extract remote sensing data at validated land cover locations, train a supervised machine learning model (XGBoost), and apply it across an entire satellite scene to monitor invasive plant distribution and clearing efforts.

## Prerequisites

We strongly recommend completing the [Intermediate training module](https://github.com/TNC-Geospatial-Conservation-Tech/ocs-2026-training/tree/main/2_Intermediate) for our data science training before taking on this Advanced module. You should also have completed the preceeding lessons in the advanced module.

## About

### Aims

This notebook demonstrates a complete end-to-end workflow for mapping invasive species across large geographic areas using cloud-native geospatial tools and supervised machine learning. The specific objectives are:

- Learn how to discover and access satellite imagery from cloud-based data repositories using STAC catalogs
- Extract spectral information from satellite data at validated field locations
- Train a machine learning classifier (XGBoost) to distinguish invasive species from other land cover types
- Deploy the trained model efficiently across entire satellite scenes using parallel processing
- Generate spatially-explicit predictions of invasive species distribution for conservation planning

### Structure

The notebook is organized into a data pipeline with three main phases:

1. **Data Preparation** (Sections 2-5): Load validation data, search for and retrieve Sentinel-2 imagery from AWS, and extract spectral features at known locations
2. **Model Development** (Section 6): Train and validate an XGBoost classifier using hyperparameter tuning and cross-validation
3. **Deployment & Export** (Section 7): Apply the trained model across the entire study area using parallel processing and export results as a cloud-optimized GeoTIFF

The example focuses on mapping invasive Pine trees in the Greater Cape Town water fund area, demonstrating how these techniques can support conservation monitoring and resource management decisions.

### TNC Contributors for 2026 Spatial Data Science virtual training - Advanced Module

<a href="https://github.com/f-tonini"><img src="https://avatars.githubusercontent.com/u/1470540?v=4" width="50" /></a>
<a href="https://github.com/contributor2-username"><img src="https://avatars.githubusercontent.com/u/8463334?v=4" width="50" /></a>

## Notebook Lesson Structure

1. Load Python packages (Xarray, GeoPandas, XGBoost, and cloud-native tools)
2. Load invasive plant and land cover validation data
3. Search for remote sensing data using STAC (Sentinel-2 L2A)
4. Load and process satellite imagery from cloud storage
5. Extract spectral data at validation point locations
6. Train a supervised machine learning model (XGBoost with hyperparameter tuning)
7. Apply the trained model across the entire study area
8. Export results as a cloud-optimized GeoTIFF

## Running the Notebook

You will be running this Notebook directly inside your own Jupyter Notebook in [SageMaker Studio Lab](https://studiolab.sagemaker.aws/). Make sure to check out the ["Getting Started with Jupyter"](https://foundations.projectpythia.org/foundations/getting-started-jupyter) content from the [Pythia Foundations](https://foundations.projectpythia.org) material if you are new to Jupyter or need a refresher. The notebook requires validation data (`gctwf_invasive.gpkg`) and an area of interest file (`aoi.gpkg`) to be present in the same directory. The workflow uses cloud-native data sources (AWS Open Data Registry) to retrieve Sentinel-2 imagery, so an internet connection is required.

## Key Concepts

- **STAC (SpatioTemporal Asset Catalog)**: A standardized specification for discovering and accessing geospatial datasets
- **Xarray**: Labeled multi-dimensional arrays for efficient handling of gridded data
- **Machine Learning Classification**: Using XGBoost gradient boosted trees for supervised classification
- **Parallel Processing**: Applying models efficiently across large satellite scenes using Dask
- **Cloud-Optimized GeoTIFF (COG)**: Export format for efficient cloud-based geospatial data access
