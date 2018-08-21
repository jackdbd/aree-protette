# Sites of Community Importance in Tuscany (Aree Protette)

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/jackdbd/aree-protette/master)

Exploratory data analysis and visualization of a small geospatial dataset with geoviews.

![An image showing the Sites of Community Importance in Tuscany, created with GeoViews](https://raw.githubusercontent.com/jackdbd/aree-protette/master/screenshots/sites-of-community-importance-in-tuscany.png "Sites of Community Importance in Tuscany.")

Built with:

- Geopandas
- Geoviews
- Cartopy
- Matplotlib
- Contextily


## Data

You will need to download these datasets to run the noteook.

Regione Toscana – [Limiti amministrativi](http://dati.toscana.it/dataset/amb-amm) (License: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)).

Regione Toscana – [Siti di Interesse Regionale, Siti di Importanza Comunitaria, Zone di Protezione Speciale](http://dati.toscana.it/dataset/sir) (License: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)).


## Run the notebook with Binder
[Binder](https://github.com/jupyterhub/binderhub) builds a docker image from a git repository + commit, so you can run the notebook `aree-protette.ipynb` in the cloud, without installing anything on your machine.


## Installation

If you want to run the notebook locally, you need to create a conda environment. The easiest way to obtain the conda package manager is to install a Python distribution like [Miniconda](https://conda.io/miniconda.html) or [Anaconda](https://repo.continuum.io/). I like Miniconda.

You can create a conda environment, install all the required dependencies, and activate the environment in two ways.

```shell
# option 1: use the environment.yml file
conda create --file environment.yml
source activate aree-protette
```

```shell
# option 2: create a new empty environment
conda create --name aree-protette python=3.6 --yes
source activate aree-protette
conda install -c pyviz geoviews -y
conda install -c conda-forge contextily -y
```

*Note:* installing all the required dependencies might take a while, go grab a cup of coffee :coffee:


## Usage

When all dependencies have been installed, run the notebook:

```shell
jupyter notebook
```


## Other

You can freeze your environment with:

```shell
conda env export > environment.yml
```

To remove this conda environment, run:

```shell
conda env remove -n aree-protette
```
