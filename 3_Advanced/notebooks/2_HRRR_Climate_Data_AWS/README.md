# HRRR Climate Data (AWS)

![thumbnail](img/thumbnail.svg)

In this module, you will access and create a map from archived data from NCEP's High-Resolution Rapid Refresh (HRRR) model, which is served in a public S3 bucket on AWS.

## Prerequisites

We strongly recommend completing the [Intermediate training module](https://github.com/TNC-Geospatial-Conservation-Tech/ocs-2026-training/tree/main/2_Intermediate) for our data science training before taking on this Advanced module.

## Motivation

This cookbook provides the essential materials to learning how to work with gridded NCEP model output that is served on AWS' S3 buckets, in a data format called Zarr.

Once you go through this material, you will have mastered the following skills:

1. Understand what *object store* refers to, and how it relates to AWS's S3 buckets

2. Familiarized yourself with the Zarr data representation model, and why it is an optimal format for data stored on S3

3. Access, analyze, and visualize gridded fields from the HRRR

Throughout this cookbook, we build on the core foundational Python material covered in the [Foundations Book](https://foundations.projectpythia.org)

## About

This cookbook was derived and edited from the extensive knowledge base available on [Project Pythia](https://foundations.projectpythia.org). We would like to acknowledge the original author, [Kevin Tyle](https://github.com/ktyle). If you have specific questions about the inner workings of the packages used in this notebook, feel free to reach out to us directly or the original author.

### TNC Contributors for 2026 Spatial Data Science virtual training - Advanced Module

<a href="https://github.com/f-tonini"><img src="https://avatars.githubusercontent.com/u/1470540?v=4" width="50" /></a>
<a href="https://github.com/contributor2-username"><img src="https://avatars.githubusercontent.com/u/8463334?v=4" width="50" /></a>

## Structure

This cookbook will have two main sections - "Foundations" and "Example Workflows."

### Foundations

The foundational content will include:

- NCEP Model data on AWS' S3
  - an overview of how to access NCEP's real-time and archived NWP model output on AWS
  - an introduction to the Zarr data format
  - How to read in a Zarr-formatted HRRR grid with Xarray

### Example Workflows

Here, we **apply** the lessons learned in the foundational material to various analysis workflows, including everything from reading in the data to plotting a beautiful visualization at the end. We include the additional dataset-specific details, focusing on building upon the foundational materials rather than duplicating previous content.

1. Plot a map of 2-meter temperature from a past HRRR run

## Running the Notebook

You will be running this Notebook directly inside your own Jupyter Notebook in [SageMaker Studio Lab](https://studiolab.sagemaker.aws/). Make sure to check out the ["Getting Started with Jupyter"](https://foundations.projectpythia.org/foundations/getting-started-jupyter) content from the [Pythia Foundations](https://foundations.projectpythia.org) material if you are new to Jupyter or need a refresher.
