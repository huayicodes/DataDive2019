# DataDive2019
In this one-day Data Dive event organized by DataKind, I worked on the "Boston Approved Building Permits Data", the "Boston Parcel Data", and the "Boston Census Data" to find trends in energy-saving works, and to forecast future work amount.

## Motivation
A number of building infrastructure upgrades can lead to huge energy and value savings, e.g. installing solar panels, improving insulation or replacing boilers. 
If we can predict the type of improvements for different areas, we can use this information to inform policymakers or local communities to initiate changes. 

## The Data
* The [Boston Approved Building Permits data](https://data.boston.gov/dataset/approved-building-permits) <br>: building works from 2010 to date. 
  - Tagged data: other volunteers in the group tagged the dataset with the different energy-saving work tags, which include: solar, heat pump, furnace, insulation, boiler, heater, etc. 
* The [Boston Parcel data](http://bostonopendata-boston.opendata.arcgis.com/datasets/parcels-2016-data-full/data): details of land properties in Boston
* The [Boston Census data](https://factfinder.census.gov/faces/tableservices/jsf/pages/productview.xhtml?src=bkmk): metadata on Boston area populations 

## Approach
* I first plotted an interactive heatmap for each work tag. (see BU_maps.ipynb 7 heatmap.zip)
* I then used the SARIMA statistic model to forecast the trends for each work tag over the next 12-month period. (see BU_predict_by_tag.ipynb)
* Lastly, I explored the trends in for the "solar" worktype at each zip code location, and checked for potential saturation by linking up the 3 different datasets. (BU_sol_trends.ipynb)

## Deliverables
* **Interactive Heatmaps**: With the heatmaps, I can easily find zip codes with the most building work done, e.g., many solar works are done at the zipcodes 02131, 02136 & 02126. I can also zoom-in on the map to discover the exact location of smaller hotspot regions or blocks.
* **Trend forecasts**: the SARIMA model predicted that 
  * the "window", "solar", "hvac", "gas", "heat pump" & "furnace" categories are likely to increase
  * while "insulation", "boiler" & "heater" categories are likely to stay the same
* **Possible saturation** in the "solar" worktype at several zip codes: on average, one unit of property at several zip code locations have multiple works done over the years. This could indicate saturation of solar panels and is import for predicting which areas may have more solar opportunities.
 
