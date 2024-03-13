---
layout: default
---

# Day 7

Today we will look at how to plot up geochemical data!

## Sample spreadsheets

Often we will recieve data from papers, colleagues, or repositories that aren't in the format that make they most sense for our analysis. For spreadsheets, for example, there is a balance in efficiency between 1) modifying them directly in Excel or a similar piece of GUI software so they are in the format that provides the simplest ingestion by `pandas` using `read_csv` or `read_excel` and 2) passing complex arguments to those `pandas` functions so that the unmodified spreadsheet can be ingested. This balance is about saving time: sometimes you may recieve hundreds of very similar spreadsheets and the latter is best, other times it makes most sense to just do the former if it's just one spreadsheet.
Your sense for which saves you time so you can focus on the science will come with experience.

Compare the spreadsheets in this day's folder from our colleagues (Lucas and Erick have kindly passed on some data) in their unmodified and modified versions to see what I mean.

## Parametric plots

Often in geochemical analysis we collect the abundances of a list of different elements or isotopes in a set of samples. The relationships between the abundances tell us important information such as the history of boundary conditions that the samples have experienced.

When doing a first look through the samples, it is often instructive to make a grid of scatter plots, where the points are the samples, and the axes are the elements or isotopes. We have written a function `parascatter` which makes this directly for a defined subset of the list of elements or isotopes. Please take a look at that function and think about how to adapt it for your own use.

## Fits for ages

Another style of analysis is to use radioactive decay within a material to infer its age. We make this inference using the relationship between ratios of isotopes which vary over time as certain isotopes decay radioactively into another, if the decay rate is known. Today we study the Rubidium Strontium system, please take a look at the notebook for the calculation.

## Seventh notebook

See the seventh notebook example online [here](https://github.com/geomorphlab/medaes/blob/gh-pages/day7/day7.ipynb). Download the directory with the notebook and the example file directly [here](./day7/day7.zip).

## Homework

Make an equivalent notebook to the one above where you ingest your own data and plot it up nicely. Go ahead and work on your own lightning presentations and the extended abstract.