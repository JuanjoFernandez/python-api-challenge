### *04/22/2021*

- Installed CitiPy library
- Built the 500+ cities list
- Pulled all relevant data from a single request to OpenWeather
- For loop coded
- Added conditional in case a request fails

### *04/23/2021*
- Tested the request for loops
    - 35 out of 598 cities returned a 404 (not found) error, meaning there's no data available for those cities
    - 5.8% of missing data
- Added a conditional loop to ensure that the cities list meets the minimum (577 cities)
- Changed some values for quick-testing purposes
    - [X] Change back sample sizes after testing
- Cleaned the dataframe of cities witout weather information
- Appended the requested data to the dataframe
- Created, formatted Temperature vs Latitude scatterplot
- Created and formatted the rest of the scatterplots
- Created linear regression for temperature vs latitude on both hemispheres
- Fixed graphs, they now show side by side
- Graphs are now saved in png format in the [plot_images](/plot_images) folder
- Final formatting of the regression plots done
- Added all the regressions
- Cleaned dataframe now saves to [weather_data.csv](/resources/weather_data.csv)
- Changed test parameters and ran the code with the +500 cities
- Added insight to all correlations
- Data obtained from API now saves "to weather_data_timestamp.csv" for reproducibility purposes
- Added csv capability