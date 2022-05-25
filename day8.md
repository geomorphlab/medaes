---
layout: default
---

# Day 7

Today we will look at how to make a DOI-minted code and data repository!

## GitHub

[GitHub](https://github.com/) is an incredibly useful website that allows people who write code and develop software to share what they have done and work on it collaboratively. Projects are held in 'repositories' and can be public or private. A lot of the software we use in our day-to-day lives, including the Python packages we've used all workshop and even this workshop website, are created using GitHub! GitHub uses software called [Git](https://en.wikipedia.org/wiki/Git) to keep tabs on what is in directories and files, and if those things change.

Today we will tell Git to keep tabs on a directory on our local computer where our project is. We will then create a GitHub repository for it, so anyone can see the most recent upload we made. Once this is done, we can create a 'version' (i.e., what the repository looked like at a moment in time) of the repository. Then finally we can make a DOI for the version with Zenodo.

Before we start this process, we need to organise our project directory. Make sure all your code and code output is in one directory that you can navigate to via terminal. If your data contains any files over 50 MB, make sure to store your data in a child directory of the project directory, and all the code in a seperate child directory. Ideally you wouldn't have to do this, but GitHub has a 50 MB limit on any given file's size.

Next we need to install Git on our computer if we don't have it already. [Here](https://github.com/git-guides/install-git) is a tutorial for installing Git on various operating systems. Then we need to create a GitHub account if we don't have one already. You can do that [here](https://github.com/join). 

After that, we can follow [this tutorial](https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github#adding-a-local-repository-to-github-using-git) to get our local directory uploaded to GitHub as a repository. 

## Zenodo

[Zenodo](https://zenodo.org/) is a file sharing website for research. Since Zenodo has the proper infrastructure and policies in place, they are able to issue Digital Object Identifiers (DOIs) to data and code stored on and accessed through the website. 

[DOIs](https://www.doi.org/) are permanent addresses for digital assets. They are the widely-adopted way we keep track of all published research articles, and since nowadays none of us read publications from a journal's printed issue, they are much more powerful way of referencing published research. Giving your code and data a DOI, in addition to your articles, is one way for other researchers to know exactly how you did your science and it makes them able to cite it if required. In the last few years a lot of journals in Earth Sciences have started requiring that code and data accompanying an article are not only publicly available, but also have a DOI.

We can use Zenodo without GitHub, but since GitHub allows us to easily upload and track changes in our project directory, and Zenodo allows us to give our code a DOI, they work very well together. 

Now we have our GitHub repository up and running, we can follow [this guide](https://docs.github.com/en/repositories/archiving-a-github-repository/referencing-and-citing-content) to give it a DOI via Zenodo.


## Homework

Once your project is finalised, create its own GitHub repository, and a DOI for a version of it using Zenodo. Go ahead and work on your own lightning presentations and the extended abstract.