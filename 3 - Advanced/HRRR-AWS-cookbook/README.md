# HRRR on AWS Cookbook

<img src="thumbnail.svg" alt="thumbnail" width="400"/>

[![DOI](https://zenodo.org/badge/507993773.svg)](https://zenodo.org/badge/latestdoi/507993773)

In this Project Pythia Cookbook, you will access and create a map from archived data from NCEP's High-Resolution Rapid Refresh (HRRR) model, which is served in an S3 bucket on AWS.

## Prerequisites
We strongly recommend completing the Intermediate training module for our data science training before taking on this Advanced module. It is also recommended that you familiarize yourself with the [Xarray](https://docs.xarray.dev/en/stable/) python library. You can use this [Introduction to Xarray](https://foundations.projectpythia.org/core/xarray/xarray-intro/) online training by Project Pythia.  

## Motivation
This cookbook provides the essential materials to learning how to work with gridded NCEP model output that is served on AWS' S3 buckets, in a data format called Zarr.

Once you go through this material, you will have mastered the following skills:

1. Understand what *object store* refers to, and how it relates to AWS's S3 buckets
1. Familiarized yourself with the Zarr data representation model, and why it is an optimal format for data stored on S3
1. Access, analyze, and visualize gridded fields from the HRRR

Throughout this cookbook, we build on the core foundational Python material covered in the [Foundations Book](https://foundations.projectpythia.org)

## Authors

This notebook was slightly edited by [Francesco Tonini](https://github.com/f-tonini) and [Glenn Moncrieff](https://github.com/GMoncrieff) from its original form. We would like to acknowledge the original author, [Kevin Tyle](https://github.com/ktyle). If you have specific questions about the inner workings of the packages used in this notebook, feel free to reach out to us directly or the original author.

### TNC Contributors for OCS 2026 Data Science Training

<a href="https://github.com/f-tonini">
  <img src="https://avatars.githubusercontent.com/u/1470540?v=4" width="80" />
  <img src="https://avatars.githubusercontent.com/u/8463334?v=4" width="80" />
</a>

### Original Contributors at Project Pythia

<a href="https://github.com/ProjectPythia/HRRR-AWS-cookbook/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ProjectPythia/HRRR-AWS-cookbook" />
</a>

## Structure
This cookbook will have two main sections - "Foundations" and "Example Workflows."

### Foundations
**Currently under development** 
The foundational content will include:
- NCEP Model data on AWS' S3 
  - an overview of how to access NCEP's real-time and archived NWP model output on AWS
  - an introduction to the Zarr data format
  - How to read in a Zarr-formatted HRRR grid with Xarray

### Example Workflows
Here, we **apply** the lessons learned in the foundational material to various analysis workflows, including everything from reading in the data to plotting a beautiful visualization at the end. We include the additional dataset-specific details, focusing on building upon the foundational materials rather than duplicating previous content.

1. Plot a map of 2-meter temperature from a past HRRR run
1. **Currently under development** Plot a time series of wind speed from a past HRRR run
1. **Currently under development** Plot a sequence of forecast maps for the most recent run of the HRRR

## Running the Notebooks
The [Jupyter Notebook document](notebooks/example-workflows/plot-2mt.ipynb) for this section can be found inside the *notebooks > example-workflows* subfolder. You will be running this Notebook directly inside your own Jupyter Notebook in [AWS SageMaker AI Studio](https://aws.amazon.com/sagemaker/ai/?trk=ceaf07a2-36ab-4fba-b62f-bcf6c48ca9f2&sc_channel=ps&trk=ceaf07a2-36ab-4fba-b62f-bcf6c48ca9f2&sc_channel=ps&ef_id=Cj0KCQiApfjKBhC0ARIsAMiR_ItWNogcywkt0EhUJePZx8eK2SY4CptBGWsPkGIADsk8OoXOyZ58dKoaAkq0EALw_wcB:G:s&s_kwcid=AL!4422!3!724218586019!e!!g!!aws%20sagemaker%20ai&gad_campaignid=19852662230&gclid=Cj0KCQiApfjKBhC0ARIsAMiR_ItWNogcywkt0EhUJePZx8eK2SY4CptBGWsPkGIADsk8OoXOyZ58dKoaAkq0EALw_wcB). Make sure to check out the ["Getting Started with Jupyter"](https://foundations.projectpythia.org/foundations/getting-started-jupyter) content from the [Pythia Foundations](https://foundations.projectpythia.org) material if you are new to Jupyter or need a refresher.
