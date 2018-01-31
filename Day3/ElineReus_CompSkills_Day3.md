
# Description of WeatherData.csv

### Data Source: 

**Main source:** 
Except as noted, U.S. National Oceanic and Atmospheric Administration (NOAA), National Weather Service (NWS), Office of Climate, Water, and Weather Services, Natural Hazard Statistics, monthly.

**Sources they used:**
1. U.S. National Weather Service, <http://www.spc.noaa.gov/climo/torn/monthlytornstats.html>. A violent, rotating column of air descending from a cumulonimbus cloud in the form of a tubular- or funnel-shaped cloud, usually characterized by movements along a narrow path and wind speeds from 100 to over 300 miles per hour. Also known as a "twister" or "waterspout."  					
2. Tropical cyclones include depressions, storms and hurricanes. For data on individual hurricanes, see the National Hurricane Center Internet site at <http://www.nhc.noaa.gov/>.										


### Data cleaning steps and other noteworthy aspects: 

1. Transpose the data, the columns become rows and rows become columns (could not manage to do this in OpenRefine, unfortunately). 
2. Change names of columns that exist more then once to names that include the weather types that are empty columns now. 
3. Remove the empty columns with weather types, as they are not useful. 
4. Then check if there are cells with errors or whitespace, there were no. 
5. Change all cells to numerical, as they all only contain numbers. For this some commas in numbers higher than 1000 should be deleted, this is done using 'replace(value, ",", "")' in the option transform. 
6. It is already well sorted by year, it is thus not necessary to sort it again. 

### Explanation of columns in the file: 

* The file is sorted using the column 'years'. 
* In the file the names of the colums start with the weather type they are about (for example: 'heat' or 'North Atlantic tropical cyclones'. After this there is written about which effect the numbers in the colomn are (such as 'number of injuries' or 'deaths') or something that gives information about for example the amount of times that weather event happened (such as 'number). 
* Weather types with their effects as they exist in the table: 
*Tornadoes*: Number, Lives lost (total), Injuries, Property loss in US (millions of dollars).
*Floods*: Lives lost, Injuries, Property loss in US (millions of dollars).
*North American tropical cyclones*: Number, Number of hurricanes, Lives lost, Property loss (billions of dollars). 
*Pacific Basin tropical cyclones*: Number, Number of hurricanes. 
*Extreme temperatures:* Lives lost (total), Injuries, Property loss in US (millions of dollars).
*Cold:* Lives lost (total), Injuries, Property and Crop loss in US (millions of dollars). 
*Heat:* Lives lost (total), Injuries, Property and Crop loss in US (millions of dollars).
*Lightning:* Death, Injuries. 



	