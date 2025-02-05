Repository to estimate life expectancy in the USA of the year 2010 where values in a particular county is calculated by using interpolation from the 3 dimensional NetCDF data. The process is to take 10 pair of latitude and longitude from the geometry column of shapefile. Xarray then interpolates the values of the variables in a set of 100 points. (1 latitude is also permuted with rest of the other 9 longitudes). The ddescription of the files:
- single_county.ipynb: finds the values of the variables in a single county by interpolating from a gridded NetCDF data.
- all_counties: finds the values of the variables in all the counties.
- combine_LE.ipynb: combine the variable dataset with the life expectancy data.
- random_forest.ipynb: results of estimating life expentancy.
- feature_engineering.ipynb: finds the fraction of time in all the counties where the 2 meter temperature was above a certain threshold.

Data

- 2010_data_interpolated.pkl: Dataframe consisting of the counties with the corresponding variables and the mean life expectancy. Use pd.read_pickle('2010_data_interpolated.pkl') to read the dataframe.

ML files

- random_forest.ipynb: notebook to estimate the life expectancy.