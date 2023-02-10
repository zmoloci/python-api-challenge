# Python API Challenge

## Finding the perfect February getaway destination:
### Using [citipy Python Library](https://pypi.python.org/pypi/citipy) and [OpenWeatherMap API](https://openweathermap.org/api) to analyze weather patterns and their correlation to latitude.

For this challenge, two separate scripts were created:
1. [WeatherPy.ipynb](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/WeatherPy.ipynb)
  - A randomized list of cities was created 
    - First, a list of randomly chosen latitude/longitude coordinates was generated.
    - This coordinate list was then used with the [citipy Python Library](https://pypi.python.org/pypi/citipy) to generate a list of cities           nearest to the random coordinates
    - The [OpenWeatherMap API](https://openweathermap.org/api) was then accessed to provide a series of meteorological measures for each city.
    - In order to begin analysis of the correlation between the meteorological measurements and latitude, four scatter plots were generated           using [MatPlotLib](https://matplotlib.org/)





2. [VacationPy.ipynb](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/VacationPy.ipynb)
  - 
  - The list of cities was then filtered down based on a series of ideal meteorological values (e.g. 
  - 
