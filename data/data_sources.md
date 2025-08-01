# Data Sources

Data files are separated into three parts:
* raw data, as received from the source
* processed data, which we have work with
* final data, fully processed data which we built our models on

## `raw` Directory


* `./raw/extreme_temperature_deaths_annual_number.csv`
	* Number of people killed globally in extreme temperature events during a given year.
	* Downloaded from GapMinder (primary source: [EM-DAT](https://www.emdat.be/database).  
	* Downloaded by Erin on July 22, 2025.  This file is NOT the original source (other files should be used instead).

* `./raw/emdat_extreme_temperature_deaths_2000_2025.xlsx` (original form), also saved as `./raw/emdat_extreme_temperature_deaths_2000_2025.csv`, downloaded from EM-DAT, The International Disaster Database, Centre for Research on the Epidemiology of Disasters (CRED), part of University of Louvain (UCLouvain), Brussels, Belgium
	* [Data documentation](https://doc.emdat.be/docs/data-structure-and-content/glossary/meteorological-hazards/)
	* [Main Website](https://www.emdat.be/)
	* Data downloaded by Erin on Tuesday, July 22, 2025

* `emdat_extreme_temp_1900_2025.xlsx`, downloaded from EM-DAT, The International Disaster Database, Centre for Research on the Epidemiology of Disasters (CRED), part of University of Louvain (UCLouvain), Brussels, Belgium
	* [Data documentation](https://doc.emdat.be/docs/data-structure-and-content/glossary/meteorological-hazards/)
	* [Main Website](https://www.emdat.be/)
	* Data downloaded by Sehar on Wednesday, July 23, 2025

* External files: global temperature data from ERA5, example file: `./raw/reanalysis-era5-land-timeseries-sfc-2m-temperatureob3k65l0.csv`
	* ERA5 Land hourly time-series data from 1950 to present [Climate Data Store, Copernicus satillite](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-land-timeseries?tab=download)
	* Data downloaded by Erin on Friday -- Saturday, July 25 -- 26, 2025
	* Full data files are available on [Google Drive](https://drive.google.com/drive/folders/1yC7wn5CA4mjju9ALo66O8LhqpOVXBVr7?usp=drive_link).  They are currently compressed in a zip file.  When uncompressed, it takes up over 2 GB.

* `number_of_deaths_per_year.csv`
	* SOURCE, include linke
	* Downloaded by XXX on XXXX


* `population.csv`
	* SOURCE, include linke
	* Downloaded by XXX on XXXX

* `world_population.csv`
	* SOURCE, include linke
	* Downloaded by XXX on XXXX





## `processed` Data Directory
Data that has been processed by the team in any way.  These are primarily data that have been partially cleaned to allow the team to save their progress.


### `daily_temperature_grid` Directory
* file name structure: `temp_lat={latitude}_long={longitude}.csv`
	* Daily summaries by latitude and longitude with mean, maximum, and minimum temperatures reported.
	* Processed by Erin
	* From ERA5 data



### `death_percentages` Directory 
* `all_disasters_reorg_2020-2024`
	* EM-DAT disasters data organized by disaster subgroup, disaster type, disaster subtype to determine the scale of extreme temperature event compared to all disasters
	* Processed by Sehar
	* EM-DAT

* `countries_reporting_all_disasters_2020-2024.csv`
	* List of all countries and their frequency annually that reported a disaster in the previous 5 yrs.  172 Nations have reported, though there are 190+ countries
	* Processed by Sehar
	* EM-DAT

* `countries_reporting_all_disasters_months_2020-2024.csv`
	* List of all countries and how many months a disaster was reported in the previous 5 yrs. Some nations report significantly more than others
	* Processed by Sehar
	* EM-DAT

* `countries_reporting_extemp_disasters_2020-2024.csv`
    * List of countries only reporting extreme temperature events in the past 5 yrs.  There are only 19 countries.
    * Processed by Sehar
	* EM-DAT
      
* `death_percentage2_location_ext_temp_2020-2024.csv`
    * Death percentage due to extreme temperature events calculated from total deaths caused by any disasters from 2020=2024.  
    * Processed by Sehar
	* EM-DAT

* `death_percentage2_location_ext_temp_month_2020-2024.csv`
    * Death percentage broken down to every month a disaster occurred.
    * Processed by Sehar
	* EM-DAT 

* `only_ext_temp-reorg_2020-2024.csv`
	* Culmination of all the above to gather how many countries and how many deaths occurred in 2020-2024 due to extreme temperatures.  Only 31 events in 5 yrs
	* Processed by Sehar
	* EM-DAT


### `extreme_temp` Directory
* `cold_deaths_reported.csv`, `heat_deaths_reported.csv`
	* lightly processed version of the EM-DAT data, for extreme cold and heat events respectively
	* processed by Erin

* `cold_events.csv`, `heat_events.csv`
	* events when minimum (or maximum) temperature was at least 2.5 standard deviations below (or above) the average temperature for that location for at least 2 days, regardless of season
	* based on the ERA5 data
	* processed by Erin

* `cold_waves.csv`, `heat_waves.csv`
	* (older version) events when minimum (or maximum) temperature was at least 2.5 standard deviations below (or above) the average temperature for that location for at least 2 days, regardless of season
	* should be replaced by the `cold_events.csv` and `heat_events.csv` respectively
	* based on the ERA5 data
	* processed by Erin 

* `extreme_temp_2020_2025.csv`
	* all days and locations when the minimum (or maximum) temperature was at least 2.5 standard deviations below (or above) the average minimum (or maximum) temperature for that location
	* based on the ERA5 data
	* processed by Erin

* `locations_lat_long.csv`
	* approximate latitude and longitude for all countries who reported deaths due to extreme temperatures to EM-DAT
	* processed by Erin

* `unique_coordinates.csv`
	* unique sets of latitude and longitude that experienced extreme minimum or maximum temperatures according to the ERA5 temperature data
	* processed by Erin




### `other` Directory
* `filename`
	* description
	* Processed by XXX
	* data sources

* `filename`
	* description
	* Processed by XXX
	* data sources




### `temp_events_grid` Directory
* Monthly summaries: `monthly_summary_lat={latitude}_long={longitude}.csv`
	* contains an average by month of that location's daily mean, maximum, and minimum temperatures.  As well as the standard deviation of the maximum and minimum daily temperature.  These are used to calculate the extreme minimum and maximum temperatures.
	* Processed by Erin
	* From the ERA5 data

* Extreme temperature days: `temp_waves_lat={latitude}_long={longitude}.csv`
	* daily records for days above the extreme maximum temperature or below the extreme minimum temperature
	* Processed by Erin
	* From the ERA5 data




## `final` Data Directory
Data in its final form and ready for modeling.  Date the file was finalized means that any future improvements or corrections are saved in another file.

* `cold_final_dataset.csv`
	* training data: deaths due to cold waves as reported to EM-DAT, combined with approximate latitude and longitude and the change in temperature from the extreme minimum temperature
	* Processed mostly by Erin. 
	* Finalized: Wed, July 30, 2025

* `final.csv`
	* description
	* Processed mostly by UNKNOWN
	* Finalized: DATE

* `hot_final_dataset.csv`
	* training data: deaths due to heat waves as reported to EM-DAT, combined with approximate latitude and longitude and the change in temperature from the extreme maximum temperature
	* Processed mostly by Erin.  
	* Finalized: Wed, July 30, 2025


