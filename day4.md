---
layout: default
---

# Day 4

Today we will look at how to plot a power spectrum and use FFTs to find patterns!

## Power spectra

Power spectra are an important tool for understanding what the dominant modes of variability are in a system. They can be used spatially to find out what wavelengths patterns occur on, or temporally to find out what timescales drive a response in a system. We will use the package `scipy` and it's sub-package `signal`, but there are other ways to do this!

In the notebook, we look at a power spectra for some example data, and we also use linear best fit to produce a powerlaw best fit to a sub-set of frequencies.

### Power law fit

We use the power law fit function from yesterday to look at how power decays with increasing frequency for a sub-range in our frequencies. See the notebook for the example.

### Peak modes

We find the maximum power in a spectra then find the frequency at which that occurs. See the notebook for the example.

## Spatial patterns

Fast Fourier Transforms (FFTs) are also an important tool for understanding what the dominant modes of variability are in a system. They can be used spatially to find out what wavelengths patterns occur on, or temporally to find out what timescales drive a response in a system. We will use the package `numpy` and it's sub-package `fft`, but there are other ways to do this!

In the notebook, we look at some topography for some example data, and we also use linear best fit to produce a powerlaw best fit to a sub-set of frequencies.

### 2-D FFT

We use a 2-D FFT to find the autocorrelation in some example data with some clear patterns. See the notebook for the example.

### Peak finding

We find the dominant orientation and wavelength of a two-dimensional pattern by analyzing this autocorrelation function. See the notebook for the example.

## Fourth notebook

See the fourth notebook example online [here](https://github.com/geomorphlab/medaes/blob/gh-pages/day4/day4.ipynb). Download the directory with the notebook and the example file directly [here](./day4/day4.zip).

## Homework

Make an equivalent notebook to the one above where you ingest your own data and plot the power spectra or autcorrelation if it's appropriate. If not, go ahead and work on your own lightning presentations and the extended abstract.