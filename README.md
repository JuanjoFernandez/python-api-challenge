# python-api-challenge
Python API's

## Resources
______
- This program is wrote on a Python Jupyter Notebook
    - Libraries used:
        - CitiPy by [wingchen](https://pypi.org/project/citipy/#files)
        - Numpy, json, requests, panadas, times
- The program runs requests to [OpenWeather](https://openweathermap.org/) API
    - In order to run the program you will need to get an API key yourself and paste it into the [config.py](config.py) file


## Overview
_________
- Using CitiPy I build a city list to be able to do the requests to OpenWeather API
    - In order to create the list I use a nested for that scans longitude and latitude to find the nearest cities
    - The latitude and longitude searches are generated randomly
        - Generating 50 lat/lon numbers (2500 searches) returns 370 cities
        - Generating 100 lat/lon numbers (10000 searches) returns 870 cities
        - Generating 70 lat/lon numbers (4900 searches) returns 500+ cities in several tests, will keep these parameters
- The cities list generated is used to make a series of calls to Openweather API in order to retrieve data relevant for the analysis
- It is possible now to begin plotting data to find relations between variables
    - The plot parameters take into account the variability of the data
- All the graphs are saved as a png image in the [plot_images](/plot_images) folder
- The data used for the analysis is saved in [weather_data.csv](/resources/weather_data.csv)
- If you wish to run the code witout making API calls skip to cell 5 of the jupyter notebook and follow the instrutions