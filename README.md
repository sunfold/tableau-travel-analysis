# tableau-travel-analysis
Tableau presentation of cleaned sample travel data from Kaggle.com

## Purpose
To practice data cleaning and standardization in Excel, then data analysis and presentation using Tableau.

## Access on Tableau Public
**NOTE: You can preview the story from my Tableau workbook at https://public.tableau.com/shared/KX46SMJWF?:display_count=n&:origin=viz_share_link.**
However, the workbook was optimized to be viewed via Tableau software.

## Project Overview
I downloaded a Kaggle.com dataset in CSV format (see kaggle-travel-dataset-original.csv in repository files) from https://www.kaggle.com/datasets/rkiattisak/traveler-trip-data. 
The dataset is a LLM-generated sample published by Kiattisak Rattanaporn. 
I cleaned the data using Excel, then imported the cleaned CSV into Tableau.
In the Tableau workbook, I created multiple sheets as well as a dashboard and story.
KPIs measured in the Tableau workbook include: 
* Aggregated spending per gender and nationality
* Most visited cities
* Change in median trip durations broken down by months across multiple years

## The Data
The cleaned dataset consists of a single CSV file comprised of 13 fields containing 137 records.
Important fields include:
* Customer demographics (nationality, age, gender)
* Travel destination
* Travel start dates and end dates
* Duration of each trip
* Cost of transportation and accommodation
* Accommodation type and transportation method 

## Data Cleaning
Data cleaning included the following steps:
1. Removed 2 null records that only contained trip ID
2. Standardized the nationality field to match country names
3. Added countries to destinations where only a city name was present
4. Truncated currency fields by removing 'USD', because all values are in USD by default

## Limitations
Some travel destination records only contain a country, without a city. Instead of attempting to analyze travel destinations by city and country separately, I chose to focus only on the top 10 most visited cities in the Tableau dashboard.
Data on the sole traveler from New Zealand was excluded from the "Aggregated by Traveler Nationality" map view, because the accommodation cost was an extreme high outlier.

## Credits
Thanks to Kiattisak Rattanaporn at https://www.kaggle.com/rkiattisak for providing the original dataset available on Kaggle.