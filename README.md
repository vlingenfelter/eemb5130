# Final Project for Ecological Dynamics (EEMB 5130)

This is the work for my final project in Ecological Dynamics (Spring 2020). My work examines the effects of different statistical downscaling methods on ecological network extinction rate predictions.

## Software information

This project was completed with R 3.6.3 (MacOS), using `rgbif` to collect species distribution data and `biomod2` for species distribution modeling. 

## Data Collection

Species distribution data was gathered from [GBIF](gbif.org). The species distribution data gathering process is outlined in `species_distributions.Rmd`. The data I gathered is found in `./species_distributions/`. There are .csv files containing the raw latitude longitude data for each observation I used to create absence/presence rasters.

## Downscaling Methods


###### Acknowledments
Work done with the help of Dr. Tarik Gouhier for Ecological Dynamics (EEMB 5130) at Northeastern University, and with the Sustainability and Data Sciences Lab under Dr. Auroop Ganguly.