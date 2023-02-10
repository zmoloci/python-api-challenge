# Python API Challenge

## Finding the perfect February getaway destination:
### Using [citipy Python Library](https://pypi.python.org/pypi/citipy) and [OpenWeatherMap API](https://openweathermap.org/api) to analyze weather patterns and their correlation to latitude.

For this challenge, two separate scripts were created:
1. [WeatherPy.ipynb](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/WeatherPy.ipynb)
  - A randomized list of cities was created 
    - First, a list of randomly chosen latitude/longitude coordinates was generated.
    - This coordinate list was then used with the [citipy Python Library](https://pypi.python.org/pypi/citipy) to generate a list of cities nearest to the random coordinates.
    - The [OpenWeatherMap API](https://openweathermap.org/api) was then accessed to provide a series of meteorological measures for each city.
    - In order to begin analysis of the correlation between the meteorological measurements and latitude, four scatter plots were generated using [MatPlotLib](https://matplotlib.org/)
    - These scatter plots were saved as .png files in the [output_data](https://github.com/zmoloci/python-api-challenge/tree/main/WeatherPy/output_data) folder.

| Latitude vs. Temperature ([Fig.1](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig1.png)) |
| ----------- |
| ![Fig.1](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig1.png) |
| ----------- |
| Latitude vs. Humidity ([Fig.2](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig2.png)) |
| ----------- |
| ![Fig.2](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig2.png) |
| ----------- |
| Latitude vs. Cloudiness ([Fig.3](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig3.png)) |
| ----------- |
| ![Fig.3](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig3.png) |
| ----------- |
| Latitude vs. Wind Speed ([Fig.3](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig3.png)) |
| ----------- |
| ![Fig.4](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig4.png) |
| ----------- |
| ----------- |

    - Two linear regressions were then performed on each of the above scatter plots, one for cities in the northern hemisphere and one for cities in the southern hemisphere. The regression line was displayed over the scatter plot along with the regression equation.
    - These 8 new scatter plots were manually saved to the [output_data](https://github.com/zmoloci/python-api-challenge/tree/main/WeatherPy/output_data) folder as Fig5.png through Fig12.png





2. [VacationPy.ipynb](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/VacationPy.ipynb)
  - 
  - The list of cities was then filtered down based on a series of ideal meteorological values (e.g. 
  - 
