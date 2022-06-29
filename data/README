# README

The glacier elevation and mass change data comes from: https://cds.climate.copernicus.eu/cdsapp#!/dataset/insitu-glaciers-elevation-mass
The DEM data comes from: https://land.copernicus.eu/imagery-in-situ/eu-dem/eu-dem-v1.1?tab=mapview 

More information: https://www.eea.europa.eu/data-and-maps/indicators/glaciers-2/assessment

## Exploring the data

One nice toolkit for exploring csvs is csvkit. 
- Docs: https://csvkit.readthedocs.io/en/latest/tutorial/1_getting_started.html
- Repo https://github.com/wireservice/csvkit

`pip install csvkit` or `brew install csvkit` to install it globally (if you want, create a venv first)


```bash
# Look at the entire dataset
$ csvlook careser_data.csv | less -S -N

# Check the columns
$ csvcut -n careser_data.csv

# Look at specific columns
$ csvcut -c 2,4,6,7 careser_data.csv

# Look at specific colum in fancier way
$ csvcut -c NAME,SURVEY_DATE,AREA careser_data.csv | csvlook | less -S -N

# Gather some initial statistics
$ csvcut -c AREA careser_data.csv | csvstat
```

## Quick notes about the DEM tiles

TL;DR from https://land.copernicus.eu/user-corner/technical-library/eu-dem-v1-1-user-guide

EU-DEM upgrade is presented in Geotiff 32 bits format.
It is a contiguous dataset divided into 100x100 km tiles, resulting in a total of 1992 tiles of 4000x4000 pixel at 25m resolution.
The Vertical accuracy is +/- 7 meters RMSE

The height of Mt Cevedale is around 3754.1 meters
