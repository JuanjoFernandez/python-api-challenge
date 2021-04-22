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
    - First test considers a search grid of 1 degree, search takes too much time to complete
    - Search grid of 10 degrees returns 221 cities
    - A 5 degrees search grid returns 609 cities, will use this sample for calculations