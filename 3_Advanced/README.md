# Spatial Data Science virtual training - Advanced Module

## Live Training Instructions

The advanced training notebooks are small enough in size to be run via https://mybinder.org

**Please click the following badge to launch a compute environment with these notebooks:** [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/TNC-Geospatial-Conservation-Tech/ocs-training-2026-intermediate-mybinder/HEAD?urlpath=%2Fdoc%2Ftree%2F01_TNC_S3_Bucket.ipynb)

⚠️ **NOTE**: Binder instances are **ephemeral** and **no changes will be saved**. Download workbooks or follow instructions below to create a compute environment for long term use.

Please note that the this maps to a separate repo specific for usage with Binder. The source is fundamentally the same but the environment dependencies have been chosen for compatibility with Binder.

## Post Training Instructions

### Option 1

To run these notebooks in an environment such as a local workstation or TNC's AWS Sagemaker deployment you can execute the following steps from a terminal to create a `conda` environment:

1. Create the python execution environment `ocs-advanced` (first time only)

`$ conda env create -f environment.yml`

2. Activate the environment (using the provided environment.yml file)

`$ conda activate ocs-advanced`

3. Register the environment (AWS Sagemaker Only)

`$ conda init`

If prompted to close and re-open your terminal, please do so.

```bash
$ conda activate ocs-advanced
$ python -m ipykernel install --user --name=ocs-advanced --display-name "Python (ocs-advanced)"
```

You should see a message like `Installed kernelspec ocs-advanced in /home/sagemaker-user/.local/share/jupyter/kernels/ocs-advanced`

Stop and restart your AWS Sagemaker instance to see this new kernel in the jupyterlab menu.

### Option 2

If you are not ready to jump onto our enterprise deployment of AWS SageMaker, you can create a `FREE` account and use [SageMaker Studio Lab](https://studiolab.sagemaker.aws/). Please, be mindful that local storage attached to these Studio Lab instances max out at 15GB! Once you have created an account, you can launch the notebook by clicking the button below and cloning the entire repository onto that environment. During the cloning process, you will also be asked if you want to install the required packages from the environment.yml file.

[![](https://studiolab.sagemaker.aws/studiolab.svg)](https://studiolab.sagemaker.aws/import/github/TNC-Geospatial-Conservation-Tech/ocs-2026-training/blob/main/3_Advanced/notebooks/1_Intro_Xarray\Intro_Xarray.ipynb)

**NOTE: Be sure to select ‘clone entire repository’ when prompted. SMSL will also ask if you want to install required packages from environment.yml. Make sure to say YES as this environment YAML file contains all of the required Python packages to complete the training sections in the Jupyter Notebooks.**