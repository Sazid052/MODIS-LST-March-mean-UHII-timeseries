# MODIS Land Surface Temperature (LST) Analysis for Dhaka City
This script is written in Google Earth Engine (GEE) for analyzing and visualizing MODIS Land Surface Temperature (LST) data. It focuses on extracting and exporting LST data for specific regions, such as Dhaka City, over a given time period. The analysis computes the mean LST for each year from 2000 to 2024 and visualizes both spatial and temporal trends.

## Description
The code performs the following tasks:

Define Locations and Study Areas:

Two BMD_location points are defined: one for Dhaka and another for Mymensingh, which can be toggled as needed.
Several regions of interest (ROI) are imported as FeatureCollection assets, such as Dhaka Core, Dhaka City Dissolved, and buffered areas.
Load and Filter MODIS LST Data:

MODIS LST data is imported from the MOD11A1 image collection, which provides daily daytime and nighttime LST at a 1-km resolution.
The script filters the LST data to March for the years from 2000 to 2024 and selects nighttime LST bands.
Convert LST from Kelvin to Celsius:

The MODIS LST data is scaled and converted from Kelvin to Celsius using a standard conversion formula.
Visualization Parameters:

LST data is visualized using a custom color palette ranging from green (cooler temperatures) to red (warmer temperatures).
Spatial Analysis:

The code clips the LST data to the selected ROI.
It calculates and prints the minimum, maximum, and average LST values for the specified region.
Export:

The clipped LST data is exported to Google Drive for further analysis or visualization.
Temporal Analysis:

The script calculates mean LST values for each year and plots a time series chart to analyze LST trends over time.
Requirements
Google Earth Engine Account: This code is written in JavaScript for use within the Google Earth Engine Code Editor.
Instructions
Setup: Import the code into the Google Earth Engine Code Editor.

Modify the Region of Interest (ROI):

The roi variable is set to a specific region in Dhaka City by default. To analyze a different region, change the roi variable to the appropriate FeatureCollection asset. Options include:
Dhaka Core
Dhaka Surroundings
Dhaka City Dissolved
Dhaka City Buffer 3.5km
Specific blocks such as 1_Block_W, 1_Block_N, etc.
Note: Make sure that the selected roi is suitable for your analysis and that you have uploaded the necessary assets to your GEE account.
Adjust Parameters:

You can switch between daytime and nighttime LST by modifying the .select() method.
Change the date range or filter criteria as needed for your specific analysis.
Outputs
Map Visualization:

The mean LST clipped to the specified ROI is visualized on the map using satellite imagery as the basemap.
Exported Image:

The clipped LST data is exported to your Google Drive folder specified in the Export.image.toDrive() function. Modify the description and folder fields to match your needs.
Time Series Chart:

A chart of mean LST values from 2000 to 2024 is generated, showing temporal trends in LST.# MODIS-LST-March-mean-UHII-timeseries
