![Header](WeatherPy/resources/header.jpg)

## **Overview**
______
- This application is splitted in 2 jupyter notebooks
    - [WeatherPy.ipynb](WeaherPy/WeatherPy.ipynb)
        - Searches for 500+ citites based on a randomly generated latitude longitude pairs
        - Performs data analysis on weather conditions to determine correlations between geographical position and some weather variables
    - [VacationPy.ipynb](VacationPy/VacationPy.ipynb)
        - Uses the csv file generated from WeatherPy to perform some analytics on Google API's
- Libraries used:
    - CitiPy by [wingchen](https://pypi.org/project/citipy/#files)
    - Numpy, json, requests, pandas, time, matplotlib, scipy, os, IPython, datetime
- The program runs requests to [OpenWeather](https://openweathermap.org/) API
    - In order to run the program you will need to get an API-key yourself and paste it into the [config.py](WeatherPy/config.py) file
    - However, if you don't want to use your API key, skip to cell 5 of the jupyter notebook and follow the instructions, you will lose the random samples though
- The program runs requests to [Google Places](https://cloud.google.com/) API for which you will need another API-key, use it at your own discretion since Google Cloud is a paid service

## **Application Breakdown**
_________
### *PyWeather*
- Using CitiPy I build a city list to be able to do the requests to OpenWeather API
    - In order to create the list I use a nested for that scans longitude and latitude to find the nearest cities
    - The latitude and longitude searches are generated randomly
        - Generating 50 lat/lon numbers (2500 searches) returns  ~370 cities
        - Generating 100 lat/lon numbers (10000 searches) returns ~870 cities
        - Generating 70 lat/lon numbers (4900 searches) returns 500+ cities in several tests, will keep these parameters
- The cities list generated is used to make a series of calls to Openweather API in order to retrieve data relevant for the analysis
- It is possible now to begin plotting data to find relations between variables
    - The plot parameters take into account the variability of the data
- All the graphs are saved as a png image in the [plot_images](WeatherPy/plot_images) folder
- The data used for the analysis is saved in the results_csv folder as "weather_data_timestamp.csv"
- If you wish to run the code witout making API calls skip to cell 5 of the jupyter notebook and follow the instrutions
- The csv file obtained by running [WeatherPy](WeatherPy/WeatherPy.ipynb) will be used on a second program useful to determine the best city to go on vacation
### *PyVacation*
- The vacation app is on [VacationPy.ipynb](VacationPy/VacationPy.ipynb)
- The application allows the user to choose any csv file obtained in [PyWeather](WeatherPy/WeatherPy.ipynb)
- If you wish to test the application witout the +500 cities the [weather_data_test](WeatherPy/results_csv/weather_data_test.csv) file contains only 40 cities
- However, if you still want to use the +500 cities list, the hotel search is done by sampling the list to 10 cities to avoid excessive Google Places API calls