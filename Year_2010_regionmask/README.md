Repository to estimate life expectancy in the USA of the year 2010 using regionmask, where the data in a particular county shapefile is calculated using the method of masking. The description of the files:
- Single_state: find value from raster to a given state
- Multiple_State: find value from a raster to multiple states
- CONUS_State: find value from a raster to Continental USA
- Single_county: find value from a raster to a single county
- County_noregrid: find value from a raster to counties in USA without regridding the raster
- County_regridded: find value from a raster to counties in USA after regridding a raster

Data
- data_nc: is the monthly mean of the weather data from CAMS
- LE_2010: is the life expectancy data from IHME
- 2010_data.pkl: is the tabular data consisting of counties with the corresponding weather data and life expectancy as exported from the County_regridded notebook.

ML files:
- linear_regression, lasso_regression, ridge_regression, SVM_gaussian, decision_trees, random forest and Neiral_Network_MLP notebook estimate the life expectancy.

**The best results, including plots and feature importance is in the random_forest notebook**

**Note**: The process of masking only works if the shapefile covers midpoint of atleast 1 raster cell (or pixel). Thus, small shapefiles or even large shapefiles that do not cover alteast 1 midpoint of a raster will return empty value. This is also mentioned in the Single_county notebook. It is thus better to interpolate the values in a given shapefile to find values of a variable from a raster. 
