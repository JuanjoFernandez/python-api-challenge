# python-api-challenge
Python API's

## Resources
______
- This program is wrote on a Python Jupyter Notebook
    - Libraries used:
        - CitiPy by [wingchen](https://pypi.org/project/citipy/#files)
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