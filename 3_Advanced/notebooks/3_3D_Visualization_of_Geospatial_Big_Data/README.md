# 3D Visualization of Geospatial Big Data with Python `Lexcube`

In this module, you will learn how to work with `Lexcube`, a Python package for data visualization in the space-time domain!

![Lexcube Logo](img/lexcube-logo.png)

![Lexcube Demo GIF](https://raw.githubusercontent.com/msoechting/lexcube/main/readme-media/lexcube-demo.gif)

--- 

**GitHub**: [https://github.com/msoechting/lexcube](https://github.com/msoechting/lexcube)

**Paper**: [https://doi.org/10.1080/20964471.2025.2471646](https://doi.org/10.1080/20964471.2025.2471646) 

**PyPI**: [https://pypi.org/project/lexcube/](https://pypi.org/project/lexcube/)

---

**NEW with version 0.4.16**: [Craft your own paper data cube!](#print-your-own-paper-data-cube)

![Print template graphic](https://raw.githubusercontent.com/msoechting/lexcube/main/readme-media/print-template.png)

## Prerequisites

We strongly recommend completing the [Intermediate training module](https://github.com/TNC-Geospatial-Conservation-Tech/ocs-2026-training/tree/main/2_Intermediate) for our data science training before taking on this Advanced module.

## Motivation

`Lexcube` is a library for interactively visualizing three-dimensional floating-point data as 3D cubes in Jupyter notebooks. 

Supported data formats:

- `numpy.ndarray` (with exactly 3 dimensions)
- `xarray.DataArray` (with exactly 3 dimensions, rectangularly gridded)

Possible data sources:

- Any gridded `Zarr` or NetCDF data set (local or remote, e.g., accessed with S3) such as Oregon's PRISM dataset
- Copernicus Data Storage, e.g., [ERA5 data](https://cds.climate.copernicus.eu/cdsapp#!/dataset/reanalysis-era5-complete?tab=overview)
- Google Earth Engine

The example notebooks found in this module will show you how to ingest and visualize data from various possible sources listed above. Take your time to look through each notebook and translate the same workflows for your own project.

## About

This cookbook was adjusted and edited from an original Medium blog post from Feb 12, 2024 available on [Medium - Towards Data Science](https://towardsdatascience.com/3d-visualization-of-geospatial-big-data-by-lexcube-python-a57512cabd69/#:~:text=Data%20visualization%20in%20three%20dimensions%20(latitude,%20longitude,,created%20by%20merging%20hundreds%20of%20raster%20layers)). We would like to acknowledge the original author, [Mahyar Aboutalebi, Ph.D.](https://towardsdatascience.com/author/mahyar-aboutalebi/) If you have specific questions about the inner workings of the packages used in this notebook, feel free to reach out to us directly or the original author.

### TNC Contributors for 2026 Spatial Data Science virtual training - Advanced Module

<a href="https://github.com/f-tonini"><img src="https://avatars.githubusercontent.com/u/1470540?v=4" width="50" /></a>
<a href="https://github.com/GMoncrieff"><img src="https://avatars.githubusercontent.com/u/8463334?v=4" width="50" /></a>

### Original Contributor on Medium

[Mahyar Aboutalebi, Ph.D.](https://towardsdatascience.com/author/mahyar-aboutalebi/)