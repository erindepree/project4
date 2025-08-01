# Unreported Deaths Due to Extreme Temperature Events
Erin De Pree, Sehar Mehmood, Ken Muchira

## Problem Statement
Given that extreme temperature events are likely to increase with global climate change, we want to identify:

* The approximate minimum number of deaths due to unreported extreme temperature events in locations compared to data available independently for regions/locations

Given the following:
* Extreme heat and heat wave events are classified as when temp are above $97.5$% ($+2.5$ standard deviation), location specific mean, and lasting at least 2 days
* Extreme Cold/Cold Wave Events are classified as when temp are below $2.5$% ($-2.5$ standard deviation), location specific mean, lasting at least 2 days

Identification of at-risk countries/underreported countries are determined by:
* publications have mentioned Africa and Middle East as being underreported
* comparing temperature data individually available to locations/regions reporting and not reporting (i.e. identification comes from lack of presence in the international emergency database, EM-DAT)

The timeline explored will look at years 2020-2024 from EM-DAT extreme temp and the dataset of daily surface temperatures (from the ERA5 analysis) covers 2020-2024 (more data is available but is time consuming to download).


## Repo Structure

* `code` contains all Jupyter notebooks

* `data` contains all raw, processed, and final datasets

* `images` holds the most useful images

* `model_results` containts more detailed predictions

* this `README.md` document

* LICENSE to use our work



## Cleaning and Early Data Analysis
### EM-DAT data: reported deaths

### ERA5 temperature data
The ERA5 data includes a temperature measured 2 meters above the ground over all land surfaces.  The ERA5 data is available from 1950 to 6 days ago on a 1 degree latitude by 1 degree longitude around the globe.  Unfortuntely, this is an extremely time consuming to download and process (both steps were run overnight).  Therefore, we have restricted ourselves to a 10 degree latitude by 10 degree longitude grid from 2020 to mid-2025. Not all data points were above land, so we had to process all the files (over 700) to determine which were helpful and which were not.  

## Modeling
### Linear Model 

### Regularization: Ridge and LASSO

### Tree Models



## Conclusions

From the linear model, we see that at least 800 cold deaths and over 80,000 heat deaths have not been reported to EMDAT.  Underreporting is very likely to be a statistically important factor.  
