## 3D Visualization of Geospatial Big Data by Lexcube! (Python)
Learn how to work with Lexcube, a Python package for data visualization in the space-time domain!

## Authors

This cookbook was derived from an original Medium blog post from Feb 12, 2024 available on [Medium - Towards Data Science](https://towardsdatascience.com/3d-visualization-of-geospatial-big-data-by-lexcube-python-a57512cabd69/#:~:text=Data%20visualization%20in%20three%20dimensions%20(latitude,%20longitude,,created%20by%20merging%20hundreds%20of%20raster%20layers)). We would like to acknowledge the original author, [Mahyar Aboutalebi, Ph.D.](https://towardsdatascience.com/author/mahyar-aboutalebi/) If you have specific questions about the inner workings of the packages used in this notebook, feel free to reach out to us directly or the original author.

### TNC Contributors for OCS 2026 Data Science Training

<a href="https://github.com/f-tonini">
  <img src="https://avatars.githubusercontent.com/u/1470540?v=4" width="80" />
</a>

### Original Contributor on Medium

<a href="https://towardsdatascience.com/author/mahyar-aboutalebi/"> Mahyar Aboutalebi, Ph.D. 
</a>

## Table of Contents
[🌟 Introduction](#Introduction)

[🌐 Lexcube](#Lexcube)

[📰 Data](#Data)

<h2 id="Introduction">🌟 Introduction</h2>
Data visualization in three dimensions (latitude, longitude, and time) is fascinating, isn’t it? As a geospatial data scientist, I have always wanted to know the easiest way to plot a cubic dataset created by merging hundreds of raster layers. While reading my feeds on LinkedIn, I found a great Python library called Lexcube, which has recently become available for Jupyter Notebook. For additional information about Lexcube, please refer to this [article](https://www.computer.org/csdl/magazine/cg/2024/01/10274107/1R6MgauvfWg) and/or check out [Lexcube on GitHub](https://github.com/msoechting/lexcube).

First of all, I’d like to thank Miguel Mahecha for sharing that post on LinkedIn and also Maximilian Söchting and his team for developing a valuable tool for the geospatial data community. Secondly, here is a hands-on exercise to help you use this package to visualize your cubic data in a 3D plot. All the steps have been coded in Python in Google Colab and by the end of this story, you will learn how to convert your raster layers to the Xarray format and then use it in Lexcube to create a 3D plot of your data.

If, like me, you were searching for a package for 3D visualization of your data, this story is for you. I have no affiliation with Lexcube and just wanted to my experience by writing this blog post.

<h2 id="Lexcube">🌐 Lexcube</h2>
Leipzig Explorer of Earth Data Cubes, or Lexcube, is an interactive data visualization tool developed by Maximilian Söchting as a Ph.D. project under the supervision of Gerik Scheuermann and Miguel Mahecha at Leipzig University. The tool is designed to handle large Earth data cubes. The project received funding from several institutions and agencies, including the European Space Agency (ESA). In May 2022, a web version of this tool became available, and recently, the open-source Jupyter Notebook was released to the community, allowing users to have full control for visualizing the large data cubes in the time, space, and variable domains.

<h2 id="Data">📰 Data</h2>
For this exercise, we will work with two different datasets. The first one is an array generated with random numbers in arbitrary latitude, longitude, and time ranges for those of you who want to quickly test Lexcube. The second one is an Xarray of long-term air temperature layers for the US from 1981 to 2020. We will learn how to merge GeoTIFF files saved in separate files into Xarray format, which is compatible with Lexcube.

## Running the Notebook
The [Jupyter Notebook document](notebooks/example-workflows/3d_bigdata.ipynb) for this section can be found inside the *notebooks > example-workflows* subfolder. You will be running this Notebook directly inside your own Jupyter Notebook in [AWS SageMaker AI Studio](https://aws.amazon.com/sagemaker/ai/?trk=ceaf07a2-36ab-4fba-b62f-bcf6c48ca9f2&sc_channel=ps&trk=ceaf07a2-36ab-4fba-b62f-bcf6c48ca9f2&sc_channel=ps&ef_id=Cj0KCQiApfjKBhC0ARIsAMiR_ItWNogcywkt0EhUJePZx8eK2SY4CptBGWsPkGIADsk8OoXOyZ58dKoaAkq0EALw_wcB:G:s&s_kwcid=AL!4422!3!724218586019!e!!g!!aws%20sagemaker%20ai&gad_campaignid=19852662230&gclid=Cj0KCQiApfjKBhC0ARIsAMiR_ItWNogcywkt0EhUJePZx8eK2SY4CptBGWsPkGIADsk8OoXOyZ58dKoaAkq0EALw_wcB). Make sure to check out the ["Getting Started with Jupyter"](https://foundations.projectpythia.org/foundations/getting-started-jupyter) content from the [Pythia Foundations](https://foundations.projectpythia.org) material if you are new to Jupyter or need a refresher.