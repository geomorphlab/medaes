---
layout: default
---

# Day 2

Today we will get our heads around function arguments and importing data!

## Functions

### Basic function

Here's the basic function we used yesterday:
```
def fluxdirectionality(dp,rdp):
     return rdp/dp
```
This function takes two variables and returns one variable (the ratio of the two input variables).


Packages like NumPy have functions like this. We call those functions within the packages like so:
```
import numpy as np
a = [1,2,3] 
np.sum(a)
```
On the first line we import NumPy so that we're able to use the package. We import it as `np` so we don't have to type out `numpy` every time we call a function from it. To use a function from NumPy, say `sum`, we use the syntax `np.sum`. The line `np.sum(a)` will return the sum of the values in the array `a`, i.e. it will return `6`.

### Positional function arguments

In the basic function `fluxdirectionality` we defined above, both the arguments `dp` and `rdp` are necessary arguments, and their order matters. For this reason, these types of arguments are called positional arguments. In `np.sum` the positional argument is `a`. If you try to run a function without all the positional arguments, it will not work.

### Default function arguments

In our function `fluxdirectionality` above, we define it such that it takes two arguments, `dp` and `rdp`. If we tried to use `fluxdirectionality` without giving it two arguments exactly, we would get an error. 


Above we used `np.sum` with just one argument, `a`. Unlike our function `fluxdirectionality`, though, `np.sum` can actually take more than one argument. Take a look at the documentation for NumPy `sum` [here](https://numpy.org/doc/stable/reference/generated/numpy.sum.html). Note how on the documentation, `np.sum` takes `a` as a positional argument, but it takes other arguments like `axis` that are defined with default values.


We can demonstrate this with the following code snippet:
```
a  = [[1,2,3],[4,5,6]]
y1 = np.sum(a)
y2 = np.sum(a,0)
```
In `np.sum`, `axis` is the first default argument. It has a default value of `None`, which for the way `np.sum` is defined, means that the sum will be for the entire matrix `a`. If we give `axis` the non-default value of `0`, `np.sum` will return the sum of `a` along its zeroth axis, and the output will have dimensions of the other axes. Default arguments are also ordered; you cannot define 'dtype', the second default argument in `np.sum`, without first defining `axis`, unless you explicitly write it out, e.g. `np.sum(x,dtype='int')`.


We can define a function ourselves that takes default values:
```
def cartesian_to_polar(x,y,thetaunit='rad'):
    r = (x**2+y**2)**0.5
    theta = np.arctan2(y,x)
    if thetaunit=='rad':
        theta = theta
    elif thetaunit=='deg':
        theta = theta*180/np.pi
    return r,theta
```
In this function, if we don't define `thetaunit` when we call `cartesian_to_polar`, it will return `theta` in radians, but if we define it as `deg`, `theta` will be returned in degrees. An example using this function is in the notebook below.

### Arbitrary function arguments

You'll see in the documentation for `np.sum` that all the variables other than `a` are default arguments; they all have default values defined for them with an equals sign in the function argument. There is a third argument type, arbitrary arguments. Arbitrary arguments do not necessarily need to be defined, can't be defined without declaring their variable, and can be defined in any order after the positional arguments and any defined non-default default arguments. An example of a function like this is the matplotlib function `scatter`. The documentation for `scatter` is [here](https://matplotlib.org/3.5.0/api/_as_gen/matplotlib.pyplot.scatter.html). 

## Data types

In science we use a lot of different data types; images, tabulated data, etc. Here we discuss how to read commonly used data types into Python.

### Spreadsheets

Spreadsheet files come with extensions like .csv, .xlsx, .txt, etc. The package pandas is a very useful tool for ingesting these data types into Python. An example using the pandas function `read_csv' is in the notebook below.

### GeoTiff files

GeoTiffs are files that contain spatial data along with the metadata that defines things like the data projection, bounds, and channels. They are used a lot in Earth Sciences for things like satellite imagery and maps.


To open a GeoTiff in Python, we can use [GDAL](https://gdal.org/). GDAL is code in the language C, but there is a Python wrapper for it.


We need to install GDAL. For pip on Windows use this [tutorial](https://opensourceoptions.com/blog/how-to-install-gdal-for-python-with-pip-on-windows/). For conda on Windows use this [tutorial](https://opensourceoptions.com/blog/how-to-install-gdal-with-anaconda/). For pip on Mac, install [brew](https://brew.sh/) then run these commands in terminal:
```
brew install gdal
pip install GDAL==3.5.0
```

We then import GDAL into Python using the command:
```
from osgeo import gdal
```

An example using the gdal function `Open' is in the notebook below.


### NetCDF files

NetCDF files can contain all sorts of data including spatial data and timeseries. They contain a lot of documentation about the data sources and units, as well as the data themselves. They are used a lot in Earth Sciences for things like climate model output.


To open a NetCDF file, we can use [xarray](https://docs.xarray.dev/en/stable/index.html#). xarray is a Python package. We also will need to install an engine for xarray to use to load the data.

To install xarray using pip, run this command in terminal:
```
pip install netcdf4 xarray
```

We then import xarray into Python using the command:
```
import xarray as xr
```

An example using the xarray function `open_dataset' is in the notebook below.


### MAT-files

A lot of data is generated by people in MATLAB, and these data are saved using a MAT-file, which has the extension `.mat`. If we want to load this data into Python, we can use the SciPy package. SciPy is an incredibly useful package in all of sciences; it just happens to include a function that loads `.mat` files.

To install SciPy using pip, run this command in terminal:
```
pip install scipy
```

We then import the subpackage of SciPy that includes the function to load `.mat` files into Python using the command:
```
from scipy.io import loadmat
```

An example using the SciPy function `loadmat' is in the notebook below.


## Second notebook

See the second notebook example online [here](https://github.com/geomorphlab/medaes/blob/gh-pages/day2/day2.ipynb). Download the directory with the notebook and the example files directly [here](./day2/day2.zip).

## Homework

Make an equivalent notebook to the one above where you ingest your own data and plot it.