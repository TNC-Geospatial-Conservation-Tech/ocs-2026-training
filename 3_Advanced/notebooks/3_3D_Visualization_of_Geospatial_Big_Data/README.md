# 3D Visualization of Geospatial Big Data with Python Lexcube

Learn how to work with Lexcube, a Python package for data visualization in the space-time domain!

![Lexcube Logo](img/lexcube-logo.png)

![Lexcube Demo GIF](https://raw.githubusercontent.com/msoechting/lexcube/main/readme-media/lexcube-demo.gif)

--- 

**GitHub**: [https://github.com/msoechting/lexcube](https://github.com/msoechting/lexcube)

**Paper**: [https://doi.org/10.1080/20964471.2025.2471646](https://doi.org/10.1080/20964471.2025.2471646) 

**PyPI**: [https://pypi.org/project/lexcube/](https://pypi.org/project/lexcube/)

---

**NEW with version 0.4.16**: [Craft your own paper data cube!](#print-your-own-paper-data-cube)

![Print template graphic](https://raw.githubusercontent.com/msoechting/lexcube/main/readme-media/print-template.png)

---

Lexcube is a library for interactively visualizing three-dimensional floating-point data as 3D cubes in Jupyter notebooks. 

Supported data formats:

- numpy.ndarray (with exactly 3 dimensions)
- xarray.DataArray (with exactly 3 dimensions, rectangularly gridded)

Possible data sources:

- Any gridded Zarr or NetCDF data set (local or remote, e.g., accessed with S3)
  
- Copernicus Data Storage, e.g., [ERA5 data](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-complete?tab=overview)

- Google Earth Engine ([using xee, see example notebook](https://github.com/msoechting/lexcube/blob/main/examples/4_google_earth_engine.ipynb))

Example notebooks can be found in the [examples](https://github.com/msoechting/lexcube/tree/main/examples) folder. For a live demo, see also [lexcube.org](https://www.lexcube.org).

## About

This cookbook was adjusted and edited from an original Medium blog post from Feb 12, 2024 available on [Medium - Towards Data Science](https://towardsdatascience.com/3d-visualization-of-geospatial-big-data-by-lexcube-python-a57512cabd69/#:~:text=Data%20visualization%20in%20three%20dimensions%20(latitude,%20longitude,,created%20by%20merging%20hundreds%20of%20raster%20layers)). We would like to acknowledge the original author, [Mahyar Aboutalebi, Ph.D.](https://towardsdatascience.com/author/mahyar-aboutalebi/) If you have specific questions about the inner workings of the packages used in this notebook, feel free to reach out to us directly or the original author.

### TNC Contributors for 2026 Spatial Data Science virtual training - Advanced Module

<a href="https://github.com/f-tonini">
  <img src="https://avatars.githubusercontent.com/u/1470540?v=4" width="50" />
  <img src="https://avatars.githubusercontent.com/u/8463334?v=4" width="50" />
</a>

### Original Contributor on Medium

[Mahyar Aboutalebi, Ph.D.](https://towardsdatascience.com/author/mahyar-aboutalebi/)

## 🌟 Introduction

Data visualization in three dimensions (latitude, longitude, and time) is fascinating, isn’t it? As a geospatial data scientist, I have always wanted to know the easiest way to plot a cubic dataset created by merging hundreds of raster layers. While reading my feeds on LinkedIn, I found a great Python library called Lexcube, which has recently become available for Jupyter Notebook. For additional information about Lexcube, please refer to this [article](https://www.computer.org/csdl/magazine/cg/2024/01/10274107/1R6MgauvfWg) and/or check out [Lexcube on GitHub](https://github.com/msoechting/lexcube).

These are hands-on exercise to help you use this package to visualize your cubic data in a 3D plot. By the end of this module, you will learn how to convert your raster layers to the Xarray format and then use it in Lexcube to create a 3D plot of your data.

## 🌐 Lexcube

Leipzig Explorer of Earth Data Cubes, or Lexcube, is an interactive data visualization tool developed by Maximilian Söchting as a Ph.D. project under the supervision of Gerik Scheuermann and Miguel Mahecha at Leipzig University. The tool is designed to handle large Earth data cubes. The project received funding from several institutions and agencies, including the European Space Agency (ESA). In May 2022, a web version of this tool became available, and recently, the open-source Jupyter Notebook was released to the community, allowing users to have full control for visualizing the large data cubes in the time, space, and variable domains.

## 📰 Data

For this exercise, we will work with two different datasets. The first one is an array generated with random numbers in arbitrary latitude, longitude, and time ranges for those of you who want to quickly test Lexcube. The second one is an Xarray of mean air temperature layers by [PRISM](https://prism.oregonstate.edu/downloads/) for the CONUS from 2000 to 2025. We will learn how to merge GeoTIFF files saved in separate files into a Zarr dataset and ingest that into the Xarray format, which is compatible with Lexcube.

## What is Zarr?

Gridded datasets, especially those produced by operational meteorological centers such as NCEP and ECMWF, are typically in NetCDF and GRIB formats. Zarr is a relatively new data format. It is particularly relevant in the following two scenarios:

1. Datasets that are stored in what's called *object store*. This is a commonly-used storage method for cloud providers, such as Amazon, Google, and Microsoft.

2. Datasets that are typically too large to load into memory all at once.

Xarray supports the Zarr format in addition to NetCDF and GRIB. The [Pangeo](https://pangeo.io) project specifically recommends Zarr as the Xarray-amenable data format of choice in the cloud:
>
>"Our current preference for storing multidimensional array data in the cloud is the Zarr format. Zarr is a new storage format which, thanks to its simple yet well-designed specification, makes large datasets easily accessible to distributed computing. In Zarr datasets, the arrays are divided into chunks and compressed. These individual chunks can be stored as files on a filesystem or as objects in a cloud storage bucket. The metadata are stored in lightweight .json files. Zarr works well on both local filesystems and cloud-based object stores. Existing datasets can easily be converted to zarr via xarray’s zarr functions."

## Running the Notebook

You will be running this Notebook directly inside your own Jupyter Notebook in [SageMaker Studio Lab](https://studiolab.sagemaker.aws/). Make sure to check out the ["Getting Started with Jupyter"](https://foundations.projectpythia.org/foundations/getting-started-jupyter) content from the [Pythia Foundations](https://foundations.projectpythia.org) material if you are new to Jupyter or need a refresher.
