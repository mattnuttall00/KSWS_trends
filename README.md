# Ongoing trend analyses for wildlife species in Keo Seima Wildlife Sanctuary

## Background

This repository is for the development and storage of the data and code that are used for conducting trend analyses for the wildilfe populations monitoried by WCS in Keo Seima Wildlife Sanctuary. The method and code were originally developed by Matt Nuttall (and collaborators) during his PhD. See here for the publication that describes the work: https://conbio.onlinelibrary.wiley.com/doi/pdfdirect/10.1111/csp2.614

In collaboration with Cain Agger and Olly Griffin from WCS Cambodia, we are now working on updating the code so that the results from the 2022 field season can be incorprated into the analysis.

## Code

There are two primary R scripts in this repository:

* `RFunc.r` - This script holds the three main functions that run the bootstrapping. This script is sourced from within the second script
* `CDS_trends_final.r` - This script calls the functions from the above script, runs the bootstrapping, and then runs the fitting of detection function models and GAM models for each replicate, for each species, and extracts the confidence intervals.

## Data

For the above scripts to run, you need: 

* The raw transect results from KSWS (see "Data" folder)
* A summary csv for each species with the results from the convential distance sampling (see "Data/CDS_results" folder)
* An up to date `sample.table.csv` (see "Data" folder)

## License 

I (MN) have kept this repo private because it will contain raw wildlife monitoring data (including locations), including those of threatened species. Therefore only authorised people will be allowed to access this repo. However, as the creator of this code, I am happy for it to be open source in the widest sense (hence the MIT license). Anyone is welcome to copy, share, edit, publish, and use this code for whatever purposes. Once the code has been successfully updated to include 2022 data, I would advocate for the raw data being removed, and then the repository being made public. 

## Contacts

* Matt Nuttall - mattnuttall00@gmail.com
* Cain Agger - cagger@wcs.org
* Olly Griffin - ogriffin@wcs.org
