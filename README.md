# little picture - lakes area monitored from space
<hr>

## Background on this little picture
_lake area varies across continents. These water bodies play a crucial role in local and global ecosystems_

Lakes are key indicators of climate change, capturing its effects directly and indirectly through surrounding areas. To respond and adapt to climate change effectively, we need a global and consistent record of lake data.
Satellite monitoring of lakes is vital for studying their response to climate change and tracking variations in their extent (or area), surface temperature, and ice cover (and thickness) and biogeochemical process via ‘water leaving reflectance’ over time.

https://climate.esa.int/en/little-pictures-gallery/lakes-monitored-from-space/

## Data Sources
The CLIP uses the following datasets:
- [ESA CCI LAKE DATA AVAILABILITY](https://climate.esa.int/documents/1704/lakes_cci_v2.0.2_data_availability_shp.zip)
- [World Continents](https://hub.arcgis.com/datasets/esri::world-continents/explore?location=-0.937843%2C-0.000006%2C2.64)

## Data Preparation

The data preparation phase of the notebook includes several steps:

1. **Reading Geospatial Data**: The notebook reads two files - one containing information about the world's continents and the other about the world's lakes. These files are read into GeoDataFrames.

2. **Coordinate Reference System (CRS) Management**: The notebook checks and sets the CRS of the GeoDataFrames to ensure the geographical data is correctly interpreted.

3. **Data Cleaning**: Unused columns in the GeoDataFrames are removed to keep the data concise and relevant.

4. **Spatial Join**: The lakes GeoDataFrame and the continents GeoDataFrame are spatially joined based on the geographical intersection of the data.

5. **Area Calculation**: The notebook converts the CRS to EPSG 3035 to calculate the area of each polygon in square meters, subsequently converting this to square kilometers.

6. **Data Aggregation**: The notebook groups the data by continent and calculates the sum of lake areas, the count of lakes, and the mean latitude and longitude for each continent.

7. **Data Saving**: The final prepared data is saved as a CSV file for future use.

## Data Visualization

The data visualization phase of the notebook involves creating various charts and posters to represent the lake data effectively:

1. **Lake Count Charts**: The notebook uses Altair to create a donut chart that represents the percentage of total lake count for each continent.

2. **Lake Area Charts**: Similar to the lake count charts, the notebook creates a donut chart to represent the percentage of total lake area for each continent.

3. **Bauhaus Style Posters**: The notebook takes the visualization a step further and creates Bauhaus style posters for both lake count and lake area distributions. These posters include the donut charts and also additional text elements such as a title and details.

The notebook ends with the display of these visualizations, which provide a clear and intuitive understanding of the distribution of lakes across the world's continents.

## CREDITS & LICENSE
- Idea by: [ESA Climate Office](https://climate.esa.int/)
- Processing Scripts by: [Ubilabs](https://www.ubilabs.com/)
- Visualization by: [Ubilabs](https://www.ubilabs.com/)

The code in this repository is published under [CC BY-SA 4.0 license](https://creativecommons.org/licenses/by-sa/4.0/)
