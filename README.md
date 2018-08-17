# netCDF4 Tutorial

Using the following tutorials:

https://scottwales.github.io/swc-climatedata/02-xarray/

http://xarray.pydata.org/en/stable/plotting.html

https://matplotlib.org/basemap/users/examples.html  --> For plotting data on a map

Along with https://jakevdp.github.io/PythonDataScienceHandbook/index.html --> Python Data Science Handbook by Jake VanderPlas

## Dependencies

 - Python 3.6.5
 - Anaconda: https://docs.anaconda.com/anaconda/install/mac-os, link for setting up Anaconda in macOS

 
## Conda virtual environment

> "Virtual environmets make it easy to cleanly separate different projects and avoid problems with different dependencies and version requiremetns across components."

### Using existing environment

- Go to your working directory and clone this repository
- Use the existing `environment.yml` to create your environment
	- `conda env create -f environment.yml` or
	-  `conda env create -n envName -f environment.yml` if you want a specific environment name. 
    - This command will install all the dependencies required for your project

### Setting up virtual environment from scratch 


 - `conda create -n test-env python=3.6.5 anaconda`  replace `test-env` with your own name
 - move to your working directory
 - run `source activate test-env` to start the environment
 - use `conda list --export` to list the libraries installed so far in your environment. Similar to `pip freeze`
	 - use `conda list --export > package-list.txt ` to save the packages listed. 
	 - use `conda export env -n envName > envName.yaml` to share your Conda environment with someone else. Choose your own `envName`. 
	 - If you used a prefix or a file location to create your environment instead of the default save location for env files, then following command can be used to export:
		- `conda env export -p $HOME/temp_dir/temp_env > env.yml`
 - To install packages in this environment, use the following command:
 		`conda install -n test-env xarray dask netCDF4 bottleneck`