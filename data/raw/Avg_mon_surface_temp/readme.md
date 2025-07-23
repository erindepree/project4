# Average monthly surface temperature - Data package

This data package contains the data that powers the chart ["Average monthly surface temperature"](https://ourworldindata.org/grapher/average-monthly-surface-temperature?v=1&csvType=full&useColumnShortNames=false) on the Our World in Data website.

## CSV Structure

The high level structure of the CSV file is that each row is an observation for an entity (usually a country or region) and a timepoint (usually a year).

The first two columns in the CSV file are "Entity" and "Code". "Entity" is the name of the entity (e.g. "United States"). "Code" is the OWID internal entity code that we use if the entity is a country or region. For normal countries, this is the same as the [iso alpha-3](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3) code of the entity (e.g. "USA") - for non-standard countries like historical countries these are custom codes.

The third column is either "Year" or "Day". If the data is annual, this is "Year" and contains only the year as an integer. If the column is "Day", the column contains a date string in the form "YYYY-MM-DD".

The remaining columns are the data columns, each of which is a time series. If the CSV data is downloaded using the "full data" option, then each column corresponds to one time series below. If the CSV data is downloaded using the "only selected data visible in the chart" option then the data columns are transformed depending on the chart type and thus the association with the time series might not be as straightforward.

## Metadata.json structure

The .metadata.json file contains metadata about the data package. The "charts" key contains information to recreate the chart, like the title, subtitle etc.. The "columns" key contains information about each of the columns in the csv, like the unit, timespan covered, citation for the data etc..

## About the data

Our World in Data is almost never the original producer of the data - almost all of the data we use has been compiled by others. If you want to re-use data, it is your responsibility to ensure that you adhere to the sources' license and to credit them correctly. Please note that a single time series may have more than one source - e.g. when we stich together data from different time periods by different producers or when we calculate per capita metrics using population data from a second source.

### How we process data at Our World In Data
All data and visualizations on Our World in Data rely on data sourced from one or several original data providers. Preparing this original data involves several processing steps. Depending on the data, this can include standardizing country names and world region definitions, converting units, calculating derived indicators such as per capita measures, as well as adding or adapting metadata such as the name or the description given to an indicator.
[Read about our data pipeline](https://docs.owid.io/projects/etl/)

## Detailed information about each time series


## Monthly average
The temperature of the air measured 2 meters above the ground, encompassing land, sea, and in-land water surfaces.
Last updated: January 7, 2025  
Unit: °C  


### How to cite this data

#### In-line citation
If you have limited space (e.g. in data visualizations), you can use this abbreviated in-line citation:  
Contains modified Copernicus Climate Change Service information (2025) – with major processing by Our World in Data

#### Full citation
Contains modified Copernicus Climate Change Service information (2025) – with major processing by Our World in Data. “Monthly average” [dataset]. Contains modified Copernicus Climate Change Service information, “ERA5 monthly averaged data on single levels from 1940 to present 2” [original data].
Source: Contains modified Copernicus Climate Change Service information (2025) – with major processing by Our World In Data

### How is this data described by its producer - Contains modified Copernicus Climate Change Service information (2025)?
Temperature of air at 2m above the surface of land, sea or in-land waters. 2m temperature is calculated by interpolating between the lowest model level and the Earth's surface, taking account of the atmospheric conditions. Temperature measured in kelvin can be converted to degrees Celsius (°C) by subtracting 273.15.

### Source

#### Contains modified Copernicus Climate Change Service information – ERA5 monthly averaged data on single levels from 1940 to present
Retrieved on: 2025-07-08  
Retrieved from: https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels-monthly-means?tab=overview  

#### Notes on our processing step for this indicator
- Temperature measured in kelvin was converted to degrees Celsius (°C) by subtracting 273.15.

- Initially, the temperature dataset is provided with specific coordinates in terms of longitude and latitude. To tailor this data to each country, we utilize geographical boundaries as defined by the World Bank. The method involves trimming the global temperature dataset to match the exact geographical shape of each country. To correct for potential distortions caused by the Earth's curvature on a flat map, we apply a latitude-based weighting. This step is essential for maintaining accuracy, especially in high-latitude regions where distortion is more pronounced. The result of this process is a latitude-weighted average temperature for each nation.

- It's important to note, however, that due to the resolution constraints of the Copernicus dataset, this methodology might not be as effective for countries with very small landmasses. In these cases, the process may not yield reliable data.

- The derived 2-meter temperature readings for each country are calculated based on administrative borders, encompassing all land surface types within these defined areas. As a result, temperatures over oceans and seas are not included in these averages, focusing the data primarily on terrestrial environments.

- Global temperature averages and anomalies are calculated over all land and ocean surfaces.


## Annual average
The temperature of the air measured 2 meters above the ground, encompassing land, sea, and in-land water surfaces. The 2024 data is incomplete and was last updated 08 July 2025.
Last updated: January 7, 2025  
Date range: 1940–2024  
Unit: °C  


### How to cite this data

#### In-line citation
If you have limited space (e.g. in data visualizations), you can use this abbreviated in-line citation:  
Contains modified Copernicus Climate Change Service information (2025) – with major processing by Our World in Data

#### Full citation
Contains modified Copernicus Climate Change Service information (2025) – with major processing by Our World in Data. “Annual average” [dataset]. Contains modified Copernicus Climate Change Service information, “ERA5 monthly averaged data on single levels from 1940 to present 2” [original data].
Source: Contains modified Copernicus Climate Change Service information (2025) – with major processing by Our World In Data

### How is this data described by its producer - Contains modified Copernicus Climate Change Service information (2025)?
Temperature of air at 2m above the surface of land, sea or in-land waters. 2m temperature is calculated by interpolating between the lowest model level and the Earth's surface, taking account of the atmospheric conditions. Temperature measured in kelvin can be converted to degrees Celsius (°C) by subtracting 273.15.

### Source

#### Contains modified Copernicus Climate Change Service information – ERA5 monthly averaged data on single levels from 1940 to present
Retrieved on: 2025-07-08  
Retrieved from: https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels-monthly-means?tab=overview  

#### Notes on our processing step for this indicator
- Temperature measured in kelvin was converted to degrees Celsius (°C) by subtracting 273.15.

- Initially, the temperature dataset is provided with specific coordinates in terms of longitude and latitude. To tailor this data to each country, we utilize geographical boundaries as defined by the World Bank. The method involves trimming the global temperature dataset to match the exact geographical shape of each country. To correct for potential distortions caused by the Earth's curvature on a flat map, we apply a latitude-based weighting. This step is essential for maintaining accuracy, especially in high-latitude regions where distortion is more pronounced. The result of this process is a latitude-weighted average temperature for each nation.

- It's important to note, however, that due to the resolution constraints of the Copernicus dataset, this methodology might not be as effective for countries with very small landmasses. In these cases, the process may not yield reliable data.

- The derived 2-meter temperature readings for each country are calculated based on administrative borders, encompassing all land surface types within these defined areas. As a result, temperatures over oceans and seas are not included in these averages, focusing the data primarily on terrestrial environments.

- Global temperature averages and anomalies are calculated over all land and ocean surfaces.


    