# Spatial Data Science virtual training - Intermediate Module

## Live training Instructions

The first step for this training module is to launch AWS SageMaker Studio Lab (**SMSL** hereafter) by clicking the button below and cloning the entire repository onto that environment. During the cloning process, you will also be asked if you want to install the required packages from the `environment.yml` file.

### Click the button below to launch AWS Sagemaker Studio Lab:  

**TODO:** Button is currently referencing `intermediate` branch. Ensure it is pointed to `main`.

[![](https://studiolab.sagemaker.aws/studiolab.svg)](https://studiolab.sagemaker.aws/import/github/TNC-Geospatial-Conservation-Tech/ocs-2026-training/blob/intermediate/2_intermediate/notebooks/02_AWSDataExchange_STAC.ipynb)

**NOTE: Be sure to select ‘clone entire repository’ when prompted. SMSL will also ask if you want to install required packages from environment.yml. Make sure to say YES as this environment YAML file contains all of the required Python packages to complete the training sections in the Jupyter Notebooks.**

## Post training Instructions

To run these notebooks in an environment other then Sagemaker Studio Lab (such as a local workstation or TNC's Sagemaker deployment) you can execute the following steps from a terminal to create a `conda` environment:

1) Create the python execution environment `ocs-intermediate` (first time only)

`$ conda env create -f environment.yml`

2) Activate the environment

`$ conda activate ocs-intermediate`

3) Register the environment (Sagemaker Only)

`$ conda init`

If prompted to close and re-open your terminal, please do so.

```bash
$ conda activate ocs-intermediate
$ python -m ipykernel install --user --name=ocs-intermediate --display-name "Python (ocs-intermediate)"
```

You should see a message like `Installed kernelspec ocs-intermediate in /home/sagemaker-user/.local/share/jupyter/kernels/ocs-intermediate`

Stop and restart Sagemaker space to see kernel in jupyterlab menu.