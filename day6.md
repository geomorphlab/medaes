---
layout: default
---

# Day 6

Today we will look at how to fit functions that cannot be cast as polynomials to data!

## Example lightning presentation

Before covering today's material, I will give a lightning presentation example for you. I have put my slides in today's .zip file if you want to review them while creating your own presentations.

## Gradient descent

Imagine we have a function that has two free parameters, and we want to adjust the free parameters of this function such that it best predicts some data we have. As we choose different values for these free parameters, the corresponding residual between the predicted value from the function and the actual value from our data can change. Think now of a landscape where the the x and y coordinates are the free parameters, and elevation is the value of that residual. Our aim is to find the lowest point in that landscape because it corresponds to where the difference between our prediction and the data is minimized. There are lots of ways of finding that mimimum; gradient descent is one of them (and there are lots of different ways of doing gradient descent!).

Often we know there is an equation that describes the relationship between variables we observe in our science, but we also have the issue that all the variables in that equation aren't observed and often need to be assumed. We can use gradient descent as a tool to calculate values for those unknown variables. Sometimes finding values for those unknown variables is the whole point of a project, othertimes it is a means to an end.

Today we will use the package `scipy` and it's sub-package `optimize`, but there are other ways to do this!

In the notebook, we look at finding two free paramters for a function that describes some example data, and we define a set of Python functions that allow us to find it through gradient descent.

## Sensitivity to initial conditions

This landscape described above might not have one watershed within the range of values you expect the free parameters to have. Simple gradient descent has a hard time finding the global minimum of cases like this, instead it finds the local minimum of the watershed you start your search from (the initial condition). It is good practice to check that your fitted values for free parameters aren't too sensitive to the initial values.

Here we do a sensitivity study for the initial condition to our gradient descent to ensure we have found the global minimum of our residual function. See the notebook for the example.

## Sixth notebook

See the sixth notebook example online [here](https://github.com/geomorphlab/medaes/blob/gh-pages/day6/day6.ipynb). Download the directory with the notebook and the example file directly [here](./day6/day6.zip).

## Homework

Make an equivalent notebook to the one above where you ingest your own data and fit whatever function is appropriate. Go ahead and work on your own lightning presentations and the extended abstract.