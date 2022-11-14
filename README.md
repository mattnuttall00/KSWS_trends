# Wildlife trend analyses from distance sampling data

## Background

This repository is for the development and storage of the code that is used for conducting trend analyses for the wildilfe populations monitoried by WCS in Keo Seima Wildlife Sanctuary, Mondulkiri Province, Cambodia. The method and code were originally developed by Matt Nuttall (and collaborators) during his PhD. See here for the publication that describes the work: https://conbio.onlinelibrary.wiley.com/doi/pdfdirect/10.1111/csp2.614

In collaboration with Cain Agger and Olly Griffin from WCS Cambodia, the code was updated so that the results from the 2022 field season can be incorprated into the analysis. This code can be updated or edited for future years, or for similar analyses elsewhere. This code should be easily adaptable for other studies or surveys, where the modelling of species population trends from distance sampling data is the desired outcome.

## Code

There are two primary R scripts in this repository:

* `RFunc.r` - This script holds the three main functions that run the bootstrapping. This script is sourced from within the second script
* `CDS_trends_final.r` - This script calls the functions from the above script, runs the bootstrapping, and then runs the fitting of detection function models and GAM models for each replicate, for each species, and extracts the confidence intervals.

## Environment

The code was originally developed using R version 4.0.4. The following pacakges and versions were used when developing the code:
`Tidyverse` v1.3.0
`Distance` v1.0.2
`data.table` v1.14.0
`gam` v1.20
`patchwork` v1.1.1
`DescTools` v0.99.42

## Data

For the above scripts to run, you need: 

* The raw transect results from KSWS or another study (see "Example data/data.csv" for an example) 
* A summary csv for each species with the results from the convential distance sampling (see "Example data/BSD_results" folder for example data)
* Copies of the `obs.table.csv`, `region.table.csv`, and an up to date `sample.table.csv` (see "Example data" folder)

## License 

To allow this repo to be public, we have removed all raw species data except some example data from Black-shanked douc, which are common and widespread across KSWS. All code authors are happy for the code to be open source in the widest sense (hence the MIT license). Anyone is welcome to copy, share, edit, publish, and use this code for whatever purpose. 

## Contacts

* Matt Nuttall - mattnuttall00@gmail.com
* Cain Agger - cagger@wcs.org
* Olly Griffin - ogriffin@wcs.org
