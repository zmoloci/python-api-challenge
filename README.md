# Python API Challenge

## Finding the perfect February getaway destination:
### Using [citipy Python Library](https://pypi.python.org/pypi/citipy) and [OpenWeatherMap API](https://openweathermap.org/api) to analyze weather patterns and their correlation to latitude.

For this challenge, two separate scripts were created:

## 1. [WeatherPy.ipynb](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/WeatherPy.ipynb)
  - A randomized list of cities was created 
    - First, a list of randomly chosen latitude/longitude coordinates was generated.
    - This coordinate list was then used with the [citipy Python Library](https://pypi.python.org/pypi/citipy) to generate a list of cities nearest to the random coordinates.
    - The [OpenWeatherMap API](https://openweathermap.org/api) was then accessed to provide a series of meteorological measures for each city.
    - In order to begin analysis of the correlation between the meteorological measurements and latitude, four scatter plots were generated using [MatPlotLib](https://matplotlib.org/)
    - These scatter plots were saved as .png files in the [output_data](https://github.com/zmoloci/python-api-challenge/tree/main/WeatherPy/output_data) folder.

| Latitude vs. Temperature ([Fig.1](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig1.png)) |
| ----------- |
| ![Fig.1](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig1.png) |

| Latitude vs. Humidity ([Fig.2](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig2.png)) |
| ----------- |
| ![Fig.2](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig2.png) |

| Latitude vs. Cloudiness ([Fig.3](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig3.png)) |
| ----------- |
| ![Fig.3](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig3.png) |

| Latitude vs. Wind Speed ([Fig.4](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig4.png)) |
| ----------- |
| ![Fig.4](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig4.png) |

  - Two linear regressions were then performed on each of the above scatter plots, one for cities in the northern hemisphere and one for cities in the southern hemisphere. The regression line was displayed over the scatter plot along with the regression equation.
  - These 8 new scatter plots were manually saved to the [output_data](https://github.com/zmoloci/python-api-challenge/tree/main/WeatherPy/output_data) folder as Fig5.png through Fig12.png
    
| Northern Hemisphere Latitude vs. Temperature ([Fig.5](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig5.png)) | Southern Hemisphere Latitude vs. Temperature ([Fig.6](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig6.png)) |
| ----------- | ----------- |
| ![Fig.5](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig5.png) | ![Fig.6](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig6.png) |

| Northern Hemisphere Latitude vs. Humidity ([Fig.7](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig7.png)) | Southern Hemisphere Latitude vs. Humidity ([Fig.8](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig8.png)) |
| ----------- | ----------- |
| ![Fig.7](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig7.png) | ![Fig.8](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig8.png) |

| Northern Hemisphere Latitude vs. Cloudiness ([Fig.9](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig9.png)) | Southern Hemisphere Latitude vs. Cloudiness ([Fig.10](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig10.png)) |
| ----------- | ----------- |
| ![Fig.9](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig9.png) | ![Fig.10](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig10.png) |

| Northern Hemisphere Latitude vs. Wind Speed ([Fig.11](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig11.png)) | Southern Hemisphere Latitude vs. Wind Speed ([Fig.12](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig12.png)) |
| ----------- | ----------- |
| ![Fig.11](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig11.png) | ![Fig.12](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig12.png) |





## 2. [VacationPy.ipynb](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/VacationPy.ipynb)
  - Using [hvplots.pandas](https://hvplot.holoviz.org/reference/geopandas/points.html) the cities were plotted onto an OpenStreetMap tile:

| All Sample Cities from [cities.csv](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/cities.csv) output. ([Fig.13](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig13.png)) |
| ----------- |
| ![Fig.13](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig13.png) |

  - The list of cities was then filtered down based on a series of ideal meteorological values:
    -   A max temperature lower than 27 degrees but higher than 21
    -   Wind speed less than 4.5 m/s
    -   Zero cloudiness
  - Using [hvplots.pandas](https://hvplot.holoviz.org/reference/geopandas/points.html) the filtered cities were plotted onto an OpenStreetMap tile. Functionality was included that allows the user to mouseover each city to see the name of the nearest hotel and the country name:

| Ideal February Vacation Cities filtered from [cities.csv](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/cities.csv) output with Nearest Hotel Name. ([Fig.14](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig14.png)) |
| ----------- |
| ![Fig.14](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig14.png) |


## Repo File Contents
- [README.md](https://github.com/zmoloci/python-api-challenge/blob/main/README.md)
  - This Readme file.
- [VacationPy.ipynb](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/VacationPy.ipynb)
  - Jupyter notebook file. Generates city plot and filtered city/hotel plot.
- [WeatherPy.ipynb](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/WeatherPy.ipynb)
  - Jupyter notebook file. Generates list of random cities, outputs into .csv file including: City_ID,City,Lat,Lng,Max Temp,Humidity,Cloudiness,Wind Speed,Country,Date
- [cities.csv](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/cities.csv)
  - csv file containing output from WeatherPy.ipynb. Includes columns: City_ID,City,Lat,Lng,Max Temp,Humidity,Cloudiness,Wind Speed,Country,Date
- [Fig1.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig1.png)
  - Latitude vs. Temperature Scatterplot
- [Fig2.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig2.png)
  - Latitude vs. Humidity Scatterplot
- [Fig3.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig3.png)
  - Latitude vs. Cloudiness Scatterplot
- [Fig4.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig4.png)
  - Latitude vs. Wind Speed Scatterplot
- [Fig5.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig5.png)
  - Northern Hemisphere Latitude vs. Temperature Scatterplot with Linear Regression
- [Fig6.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig6.png)
  - Southern Hemisphere Latitude vs. Temperature Scatterplot with Linear Regression
- [Fig7.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig7.png)
  - Northern Hemisphere Latitude vs. Humidity Scatterplot with Linear Regression
- [Fig8.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig8.png)
  - Southern Hemisphere Latitude vs. Humidity Scatterplot with Linear Regression
- [Fig9.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig9.png)
  - Northern Hemisphere Latitude vs. Cloudiness Scatterplot with Linear Regression
- [Fig10.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig10.png)
  - Southern Hemisphere Latitude vs. Cloudiness Scatterplot with Linear Regression
- [Fig11.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig11.png)
  - Northern Hemisphere Latitude vs. Wind Speed Scatterplot with Linear Regression
- [Fig12.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig12.png)
  - Southern Hemisphere Latitude vs. Wind Speed Scatterplot with Linear Regression
- [Fig13.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig13.png)
  - All Sample Cities from cities.csv output: using hvplots.pandas the cities were plotted onto an OpenStreetMap tile.
- [Fig14.png](https://github.com/zmoloci/python-api-challenge/blob/main/WeatherPy/output_data/Fig14.png)
  - .png file of hvplots.pandas with filtered cities plotted onto an OpenStreetMap tile. Functionality was included that allows the user to mouseover each city to see the name of the nearest hotel and the country name in Jupyter Notebook.


  
