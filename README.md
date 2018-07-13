# Aree Protette

[![Binder](https://mybinder.org/badge.svg)](https://mybinder.org/v2/gh/jackdbd/aree-protette/master)

Exploratory data analysis and visualization of a small geospatial dataset with geoviews.

![An image showing the Sites of Community Importance in Tuscany, created with GeoViews](https://raw.githubusercontent.com/jackdbd/aree-protette/master/screenshots/sites-of-community-importance-in-tuscany.png "Sites of Community Importance in Tuscany.")


## Data

You will need to download these datasets to run the noteook.

Regione Toscana – [Limiti amministrativi](http://dati.toscana.it/dataset/amb-amm) (License: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)).

Regione Toscana – [Siti di Interesse Regionale, Siti di Importanza Comunitaria, Zone di Protezione Speciale](http://dati.toscana.it/dataset/sir) (License: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/)).


## Run the notebook with Binder
[Binder](https://github.com/jupyterhub/binderhub) builds a docker image from a git repository + commit, so you can run the notebook `beni-confiscati.ipynb` in the cloud, without installing anything on your machine.


## Installation

If you want to run the notebook locally, you need to create a conda environment. You can use either [Miniconda](https://conda.io/miniconda.html) or [Anaconda](https://repo.continuum.io/).

Create and activate a new conda environment:

```shell
conda create --name aree-protette python=3.6 --yes
source activate aree-protette
```

Install all the dependencies (this might take a while, go grab a cup of coffee):

```shell
conda install -c pyviz geoviews -y
conda install -c conda-forge contextily -y
```

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
