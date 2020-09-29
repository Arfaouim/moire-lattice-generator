# Moiré lattice generator
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/TAdeJong/moire-lattice-generator/master?urlpath=lab/tree/moire-plane-wave-animation-interactive.ipynb)

Magic angle bilayer graphene was shown to be superconducting in 2018 [[1](https://doi.org/10.1038/nature26160)]. 
Despite the considerable hype concerning this discovery, little code exists to visualize the moiré pattern of two graphene layers.

To illustrate the work as done in our own paper ["Direct evidence for flat bands in twisted bilayer graphene from nano-ARPES"](https://www.nature.com/articles/s41567-020-01041-x) ([arXiv version here](https://arxiv.org/abs/2002.02289)), I created this repository.
This repository contains a simple Python notebook to interactively generate visualizations of moire patterns of hexagonal lattices at different angles.

A high resolution resulting movie can be found [here](https://www.youtube.com/watch?v=c4n1pMsDNaU).

Click the "Launch binder" button above to open an interactive notebook directly in your browser. (Note: performance in the mybinder environment is somewhat slow. Download and run the notebook on a local machine for better performance.)
![moire pattern](https://repository-images.githubusercontent.com/292806144/05106400-eeab-11ea-8e2f-0b35075b7cef)

## Local installation using conda:

- Clone the repository and open a terminal in the folder `moire-lattice-generator`
- Create the conda environment: `conda env create -f binder/environment.yml`
- Activate the environment: `conda activate moire-gen`
- Run jupyter lab: `jupyter lab` (or use a classical notebook if you prefer.)
- Update the following line in the notebook: `cluster = LocalCluster(n_workers=1, threads_per_worker=4, memory_limit='2GB')` to match your local machine. The default `cluster=LocalCluster()` typically works fine.
