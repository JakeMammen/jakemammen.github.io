## Working with Spatial Data in R

**Description:** This project uses a GIS framework to create a geoprocessing program that analyzes land suitability for wind turbines based off the impact certain factors such as environmental, ecological, cultural, human settlement, and physical infrastructure have on wind turbine placement. More specifically differences in wind speed; distances from a road network, urban areas, and differences in the topography of the land could prove to be the primary factors in determining land suitability for wind turbines across the United States. This project uses a GIS and programming approach to analyze various energy and geographic datasets. As a result, the various patterns are illustrated through the use of maps by determining wind turbine placement and in return provide some useful information for planners and engineers to aid in decision making.

## Coding examples:

In order to perform geoprocessing techniques for this particular use case, we need to download the data first and make sure it was stored in a folder on the local computer. After data collection, four different geoprocessing tools were selected to carry out the analysis.

### Import proper library and call the dataset:

```javascript
library("GISTools")
data(georgia)
plot(georgia)
```

### Create layers to visualize Urban, Suburban and Rural Counties in Georgia:

```javascript
# Create new layer for urban counties
urban_counties <- georgia[georgia$PctRural <= 10,]
plot(urban_counties)

# Create new layer for suburban counties
suburban_counties <- georgia[georgia$PctRural > 10 & georgia$PctRural < 70,]
plot(suburban_counties)

# Create new layer for rural counties
rural_counties <- georgia[georgia$PctRural >= 70,]
plot(rural_counties)
```

### Plot map:

```javascript
# Plot Georgia
plot(georgia)
# Plot the new layers with the addition of "add=T" to overlay layers
plot(urban_counties, add=T, col="orangered3")
plot(suburban_counties, add=T, col="orange")
plot(rural_counties, add=T, col="lightgoldenrod1")
title("Percentage of the county's residents classified 
      as Urban, Suburban, & Rural in Georgia     ")
legend("topright", legend=c("Urban Counties", "Suburban Counties", "Rural Counties"), 
       fill=c("orangered3", "orange", "lightgoldenrod1", border = "black"))
```

### Buffering to illustrate wind turbines relationship to airports:

```javascript
# Import system modules 
import arcpy

# Set environment or workspace settings
arcpy.env.workspace = r"C:\Users\user\folder\Term_Project_Outputs"

output_file2 = r"C:\Users\user\folder\TurbBuffer"
buffer_dist = input("Enter buffer distance: ")

# Buffer areas of aiports in Maine
turbines = "Turb_Panhandle_Counties.shp"
turbinesBuffer = output_file2
distanceField = buffer_dist
sideType = "FULL"
endType = "ROUND"
dissolveType = "ALL"

# Execute Buffer
arcpy.Buffer_analysis(turbines, turbinesBuffer, distanceField, sideType, endType, 
                      dissolveType)
print(output_file2, "Buffer Distance: ", buffer_dist)
```

## Support the selection of appropriate statistical tools and techniques (desired outcome):

<img src="/images/Buffer_Airport_Turbine_ArcMap.jpg">

## A basis for further data collection through results and conclusion:

As a result, this project provides the user a geoprocessing program with the ability to view and anlayze the various patterns in determining wind turbine placement and provide some useful information for planners and engineers to aid in decision making. For those who want to research further and continue with the project, I may suggest adding a little more detail at the local level such as road networks and local demographic information.
