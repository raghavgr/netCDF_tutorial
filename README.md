# netCDF4 Tutorial

Using the following tutorials:

https://scottwales.github.io/swc-climatedata/02-xarray/

http://xarray.pydata.org/en/stable/plotting.html

https://matplotlib.org/basemap/users/examples.html  --> For plotting data on a map

## Dependencies

 - Python 3.6.5
 - Anaconda: https://docs.anaconda.com/anaconda/install/mac-os, link for setting up Anaconda in macOS

 
## Conda virtual environment

> "Virtual environmets make it easy to cleanly separate different projects and avoid problems with different dependencies and version requiremetns across components."

 - `conda create --prefix temp/test-env python=3.6.5`
 - move to the directory `temp` where `test-env` environment was created
 - run `source activate test-env` to start the environment
 - use `conda list --export` to list the libraries installed so far in your environment. Similar to `pip freeze`
	 - use `conda list --export > package-list.txt ` to save the packages listed.  				
 - To install packages in this environment, use the following command:
 		`conda install --prefix temp/test-env xarray dask netCDF4 bottleneck`
 
