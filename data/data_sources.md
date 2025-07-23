# Data Sources

## File: `./raw/extreme_temperature_deaths_annual_number.csv`
from GapMinder.

Description: Number of people killed in extreme temperature during a given year.
Source_url: https://www.emdat.be/database


## File: `./raw/emdat_extreme_temperature_deaths_2000_2025.csv`
__Source:__ EM-DAT, The International Disater Database

Centre for Research on the Epidemiology of Disasters (CRED), part of University of Louvain (UCLouvain), Brussels, Belgium

[Data documentation](https://doc.emdat.be/docs/data-structure-and-content/glossary/meteorological-hazards/)

[Main Website](https://www.emdat.be/)

Data downloaded by Erin on Tuesday, July 22, 2025


## File: `./raw/avg_mon_surface_temp/average-monthly-surface-temperature.csv`
Temperature in degrees Celsius.

[Our World in Data](https://ourworldindata.org/grapher/average-monthly-surface-temperature?time=2024-10-15)

Data Sources: Contains modified [Copernicus Climate Change Service information](https://cds.climate.copernicus.eu/datasets/reanalysis-era5-single-levels-monthly-means?tab=overview) (2025) – with major processing by Our World in Data

Python with Pandas Code example (provided by Our World in Data)
```
import pandas as pd
import requests

# Fetch the data.
df = pd.read_csv("https://ourworldindata.org/grapher/average-monthly-surface-temperature.csv?v=1&csvType=full&useColumnShortNames=true", storage_options = {'User-Agent': 'Our World In Data data fetch/1.0'})

# Fetch the metadata
metadata = requests.get("https://ourworldindata.org/grapher/average-monthly-surface-temperature.metadata.json?v=1&csvType=full&useColumnShortNames=true").json()
```

Directory includes a `.csv` file with the data, metadate in JSON format, and a README.

Data downloaded by Erin on Wednesday, July 23, 2025