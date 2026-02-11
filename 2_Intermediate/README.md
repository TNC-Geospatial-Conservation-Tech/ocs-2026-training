# Spatial Data Science virtual training - Intermediate Module

## Live training Instructions

The intermediate training notebooks are small enough in size to be run via https://mybinder.org

**Please click the following badge to launch a compute environment with these notebooks:** [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/TNC-Geospatial-Conservation-Tech/ocs-training-2026-intermediate-mybinder/HEAD?urlpath=%2Fdoc%2Ftree%2F01_TNC_S3_Bucket.ipynb)

Note that Binder instances are ephemeral and no changes will be saved.
Download workbooks or follow instructions below to create a compute environment for long term use.

Please note that the this maps to a separate repo specific for usage with Binder.
The source is fundamentally the same but the environment dependencies have been chosen for compatibility with Binder.

## Post training Instructions

To run these notebooks in an environment such as a local workstation or TNC's Sagemaker deployment you can execute the following steps from a terminal to create a `conda` environment:

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
