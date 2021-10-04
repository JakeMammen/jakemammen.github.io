## This page will show some of my spatial programming and GIS experience

**Project description:** This project uses a GIS framework to create a geoprocessing program that analyzes land suitability for wind turbines based off the impact certain factors such as environmental, ecological, cultural, human settlement, and physical infrastructure have on wind turbine placement. More specifically differences in wind speed; distances from a road network, urban areas, and differences in the topography of the land could prove to be the primary factors in determining land suitability for wind turbines across the United States. This project uses a GIS and programming approach to analyze various energy and geographic datasets. As a result, the various patterns are illustrated through the use of maps by determining wind turbine placement and in return provide some useful information for planners and engineers to aid in decision making.

### 1. Coding examples used throughout this program:

In order to perform geoprocessing techniques for this project and throughout this program, I first had to download data and make sure it was stored in a folder on the local computer. After data collection, four different geoprocessing tools were selected to carry out the analysis.

```javascript
# Description: Perform a clip of turbines or airports taking user input

# Import system modules 
import arcpy

# Set environment or workspace settings
arcpy.env.workspace = r"C:\Users\jakem\OneDrive\Desktop\SpatialProgrammingandGIS\TermProject\TestData\All_Data"

# Ask the user for input
clip_turbine_or_airport = input("Enter Clip, Turbine or Airport?: ")

# Conditional statement to drive the script
if clip_turbine_or_airport == "Clip Turbine":
    output_file = input(r"Provide an output file name for clip: ")
    in_features = "USWindTurbines_Project.shp"
    clip_features = "USStates_Project.shp"
    out_feature_class = output_file

# Execute Clip
    arcpy.Clip_analysis(in_features, clip_features, out_feature_class)
    print(output_file)
else:
    output_file = input(r"Provide an output file name for clip: ")
    in_features = "AirportsProject.shp"
    clip_features = "USStates_Project.shp"
    out_feature_class = output_file

# Execute Clip
    arcpy.Clip_analysis(in_features, clip_features, out_feature_class)
    print(output_file)
```

### 2. Coding examples continued...

```javascript
if (isAwesome){
  return true
}
```

### 3. Support the selection of appropriate statistical tools and techniques

<img src="/images/Buffer_Airport_Turbine_ArcMap.jpg">

### 4. Provide a basis for further data collection through results and conclusion

As a result, this project provides the user a geoprocessing program with the ability to view and anlayze the various patterns in determining wind turbine placement and provide some useful information for planners and engineers to aid in decision making. For those who want to research further and continue with the project, I may suggest adding a little more detail at the local level such as road networks and local demographic information.

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).
