---
layout: default
---

# Day 7

Today we will look at how to make publication-ready figures!

## Elements

The clarity of your writing can help readers understand your science better. The same goes for figures. Common advice is that you should be able to understand the point of an article by just looking at the figures, or just reading the text; you shouldn't need both. Making aesthetically pleasing figures probably makes people want to read your paper a little more too, and I imagine it also makes editors more likely to send your manuscript out for review. With a little effort, you can write code to produce figures that convey your science well, look good, and adhere to the formatting requirements of the journal you're submitting to.

Journals often have formatting requirements for; the font and its size, the lettering for the panels, the figure's file type, dimensions and resolution. We can write code to produce figures such that they adhere to all these requirements. Today we will use the [Nature formatting requirements](https://www.nature.com/documents/Final_guide_to_authors.pdf) as an example.

## Implementation

We will use the `matplotlib` package we've been using this whole workshop to make an example publication-ready figure, but this time we will get a lot more precise with default arguments such that the end result isn't just a draft for our respective research group's eyes only. The code required to make a figure like this ends up being a lot longer, but once we've done it once, we can copy and adapt it with very little additional effort.

The first thing we do is sketch out how we want the figure to look on a piece of paper; this is our vision. Next we code it up. We have to think about where the elements of the figures sit with respect to the entire figure, and where elements of a given panel sit with respect to that panel. We want to declare variables for these locations in either reference frame (figure-wide or panel-specific) if they are in any way related to one another. This ensures that any alignment between elements is enforced.

## Seventh notebook

See the seventh notebook example online [here](https://github.com/geomorphlab/medaes/blob/gh-pages/day7/day7.ipynb). Download the directory with the notebook and the example file directly [here](./day7/day7.zip).

## Homework

Make an equivalent notebook to the one above where you ingest your own data and plot it up nicely. Go ahead and work on your own lightning presentations and the extended abstract.