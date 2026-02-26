Repository to estimate and identify factors that affect life expectancy in the USA from the year 2003 to 2019. A brief description of the list of files is below:


- Variables_detail.docs: Consists of the details about the sources of varibles, method to download and list of variables.
- Weather_prediction.yml: The environment file.
- all_years: Consists notebook to correctly interpolate raster data to boundary points of counties from raster CAMS and ERA5 data. The 2010 file consists of details including procedure for a single county, all counties, and feature engineering.
- Figures: Notebooks to plot figures
- Results: Result of estimation and feature importance.
- Notebook to create gif files of variables.
- life_expectancy_data: Consists of the life expectancy data.
- get_LE_data: notebook to get IHME unprocessed data. That is to extract total life expectancy of age group <1 year old from a set of options.
- one_year_complete: An initial attempt to interpolate life expectancy at county level for a single year. The process of interpolation was inaccurate as 10 pairs of latitude and longitude as randomly chosen leading to pairs of longitude and latitude beyond county region.
- Year_2010_interpolated: Similar to one_year_complete" file for the year 2010. These two files can be ignored.
- Year_2010_regionmask: The methodology to find values of varibles in a county was done using the regionmask package. This method was not efficient when the shapefile of the county (specially small ones) could not cover the mid-point of the raster data from CAMS. This file can be igonored.
- shapefile_sources: Word file indicating sources of shapefile
- Data: the final dataframe consisiting of environmental variables, corresponding year, fips (id to identify county) and life expectancy
