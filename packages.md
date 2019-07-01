---
layout: default
title: The RECON hub
description: R packages developed to support the RECON organisation
---

## Current packages

Here's our R packages. Most of the packages are available in [our drat repository](../drat). The [Travis CI status page](https://travis-ci.org/reconhub) can be used to check the build status of development versions (on GitHub).

| Category | Package | Available From drat | On CRAN | 
|----------|---------|---------------------|---------|
| Utility | [aweek](https://github.com/reconhub/aweek) | Yes | [![CRAN](http://www.r-pkg.org/badges/version/aweek)](https://cloud.r-project.org/package=aweek) |

Contributions are always welcome.  Pull requests via GitHub are the preferred way to contribute code and documentation. Ideas, brainstorming, and general discussion are welcome as issues on project-specific repositories or in the [RECON slack](). If you would like to contribute a new package, have a look at [the contributing page](../contributing).

## Installation Instructions

As they are released, all packages are hosted in [a drat repository](https://github.com/eddelbuettel/drat) on this website (specifically: [https://reconhub.github.io/recondrat](https://reconhub.github.io/recondrat)) and versions are updated daily and are periodically released to CRAN. This means you can install and upgrade cloudyr packages quite simply directly from R:

```R
if (!require("drat")) {
    install.packages("drat")
    library("drat")
}
drat::addRepo("recondrat", "https://reconhub.github.io/recondrat/drat")
install.packages("NameOfPackage")
```

To make this even easier, you can add `drat::addRepo("recondrat")` to your `.Rprofile` or `Rprofile.site` file, so that the recondrat repository is available every time you open R.


### Installation using devtools

You can also install packages using `remotes::install_github()` or `devtools::install_github()`. Note, however, that all stable versions of packages are automatically added to the recondrat drat, so you can always retrieve a stable version using the above workflow. To obtain a potentially unstable version, use:

```R
if (!require("remotes")) {
    install.packages("remotes")
}
remotes::install_github("reconhub/NameOfPackage")
```

## Thanks
Thanks to the [cloudyr project](https://github.com/cloudyr) for providing the basis for this repo.
