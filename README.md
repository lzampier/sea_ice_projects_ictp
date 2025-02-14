# sea_ice_projects_ictp

Repository containing useful information and scripts for the projects of the summer school on Polar Climates.

## If you are using your own laptop to analyze Icepack data or the ERA Observations

If you are lucky, `conda` is already installed in your system, either through Anaconda or Miniconda. Miniconda is a minimal installation of Anaconda, which will be enough for the scope of our project. Check if you have `conda` installed in your system by typing:

```
user@server:~$ conda
usage: conda [-h] [-v] [--no-plugins] [-V] COMMAND ...

conda is a tool for managing and deploying applications, environments and packages.

options:
  -h, --help          Show this help message and exit.
  -v, --verbose       Can be used multiple times. Once for detailed output, twice for INFO logging, thrice for DEBUG logging, four times for TRACE logging.
  --no-plugins        Disable all plugins that are not built into conda.
  -V, --version       Show the conda version number and exit.

commands:
  The following built-in and plugins subcommands are available.

etc...
```
If conda is not installed, and you are on a cluster or HPC system try `module load anaconda` or `module avail` to see if there is a conda installation available for you. If conda is still not installed, you can easily install miniconda on your platform of choice (Windows, Linux, Mac) by following [**this guide**](https://docs.anaconda.com/miniconda/). You might need to restart your shell after installing `conda`. 


## If instead you want to use the computers in the ictp info lab use the username and password that you were provided

## Run once to get stated


### Install miniconda

wget https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh

chmod 744 ./Miniconda3-latest-Linux-x86_64.sh

./Miniconda3-latest-Linux-x86_64.sh

./miniconda3/bin/conda init

source ./.bashrc




`mamba` is a reimplementation of the conda package manager in C++. To make it simple, it runs faster than `conda` and I recommend installing and using it by running 


```
conda install -c conda-forge mamba
```



## Create a new environment, we'll call it my-env but you can use whatever you want, and install the Python packages you need

Run the following commands, that should install everything you need for starting with your project.

```
conda create --name seaice

conda activate seaice

mamba install -c conda-forge xarray dask netCDF4 bottleneck matplotlib cfgrib zarr dask gcsfs cmocean ipykernel scipy jupyterlab
```


This can take up to about 20 minutes. The evolution of the installation can be monitored by a progress bar.

Install the environment in your account with

```
python -m ipykernel install --user --name seaice --display-name "Python seaice"
```


Now you should be able to run `jupyter lab` from a shell with your active environment and find all the Python packages you installed already available there.


## next time you start the computer you may need to 


```
conda activate seaice

jupyter lab &


```
