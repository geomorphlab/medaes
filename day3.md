---
layout: default
---

# Day 3

Today we will look at how to do linear regression and associated stastics!

## Line of best fit

Linear regression is an important tool in understanding how sensitive a depedent variable is to an independent variable, or to look at how variables change with respect to one another. The NumPy function `polyfit` is one way to make a linear line of best fit in Python. See the documentation [here](https://numpy.org/doc/stable/reference/generated/numpy.polyfit.html). 

In the notebook, we look at a linear best fit for some example data and we also use linear best fit to produce a powerlaw best fit.

## R-Squared

The R-squared parameter tells us how much of the variance in one variable can be explained by another variable. It is one parameter among many we can use to assess how strong the correlation is between variables. In the notebook we use the residuals from our lines of best fit to calculate the R-squared value, but this can be done automatically with functions like `linregress` in `scipy.stats`.

## Percentiles

Box-and-whisker diagrams and cumulative distributions can be cast in terms of percentiles of a variable: "what percentage of my variable is below some value?" The NumPy function `percentile` is an easy way of calculating a percentile. We don't use it in the notebook, but you can plot a box-and-whisker diagram directly in matplotlib using the `boxplot` function.

## Residual distributions

Examining the distribution of the residuals between actual data and your prediction is often a really useful way of deciding if your prediction is robust. Natural data often has some scatter in it due to measurement error, or maybe noise in the system you're studying, and so we can expect some error in your prediction even if its correct. The residuals should typically be normally distributed, and we can check if that's the case by comparing their probability density function (PDF) to a normal PDF found using their 1st (mean) and 2nd (variance) moments. This comparison can be quantified using a [Kolmogorov-Smirnoff test](https://en.wikipedia.org/wiki/Kolmogorov%E2%80%93Smirnov_test). In the notebook we create these comparisons for two fits to our data.

## Other statistics

There are MANY statistical tests, ways to fit data, and many ways to do each of them in Python; we can't cover everything and just scratched the surface of a handful of things. Other useful packages for doing all sorts of statistics are [`scipy.stats`](https://docs.scipy.org/doc/scipy/reference/stats.html) and [`sklearn`](https://scikit-learn.org/stable/). Please let your specific research areas guide you in figuring out which ones to use; hopefully this course gives you the confidence to explore things we haven't covered.

## Third notebook

See the third notebook example online [here](https://github.com/geomorphlab/medaes/blob/gh-pages/day3/day3.ipynb). Download the directory with the notebook and the example file directly [here](./day3/day3.zip).

## Homework

Make an equivalent notebook to the one above where you ingest your own data and plot distributions and linear fits to your data (where appropriate).