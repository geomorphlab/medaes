---
layout: default
---

# Day 5

Today we will look at how to make nice regularly-gridded data at the resolution we require!

## Regridding on a line

Our time-series data or spatial data like transects might come in a resolution we want to change. For example, if we're working with two datasets at different resolutions, but we want colocated pairing of these data, we need to regrid one or both. We will use the package `scipy` and it's sub-package `interpolate`, but there are other ways to do this!

In the notebook, we look at creating regularly-gridded transects at known resolution for some example data, and we create a function where we do this for 2-d spatial data at a determined angle.

## Regridding on a surface

The above ideas apply to 2-D data. We use the power of the `xarray` package to regrid spatial data stored in a `.nc` file. See the notebook for the example.

## Regridding irregularly-spaced data

Often we have data, specifically field or experiment data, where it isn't possible to collect it in a perfectly regularly grid (in time, space, or both) but to study it, we need to regrid it. An example analysis that requiring regularly-gridded data are the FFT methods we talked about last class. 

Here we take some irregularly-gridded data and use a nearest-neighbour method to re-grid it in a regular fashion. See the notebook for the example.

## Fifth notebook

See the fifth notebook example online [here](https://github.com/geomorphlab/medaes/blob/gh-pages/day5/day5.ipynb). Download the directory with the notebook and the example file directly [here](./day5/day5.zip).

## Homework

Make an equivalent notebook to the one above where you ingest your own data and grid your data if it's appropriate. If not, go ahead and work on your own lightning presentations and the extended abstract.