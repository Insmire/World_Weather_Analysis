## Overview

The purpose of this project is to generate an itinerary from real-time data which is filtered by the user's weather preference. To this end I make API calls to extract weather information, find nearest cities and hotels based on the temperature preference, then create a route between four locations which varies by transportation method.

---

## Resources

Data Source:

    OpenWeatherMap API 
    https://openweathermap.org/current

    Google Maps Places API
    https://developers.google.com/maps/documentation/places/web-service

Applications and Tools:

    Jupyter Notebook
    Pandas
    Python

---

## Results

First I randomly generate 2,000 longitude and latitude sets, then find the nearest city for each set before making an API call to OpenWeatherMap to obtain weather information for each city. The weather information include longitude, latitude, maximum temperature, percent humidity, percent cloudiness, wind speed, and description (ex. sunny, partly cloudy, etc.). This is saved in WeatherPy_Database.csv within the Weather_Database folder.

Then I filter the locations based on user input for minimun and maximun temperature. Using these locations I search for a hotel within 5000 meter of each city. The result is added to the pop-up marker of the map so that each marker contains the hotel name, city, country, current weather, and maximum temperature. The new list of locations and weather information is saved to WeatherPy_Vacation.csv in the Vacation_Search folder.

A screenshot of WeatherPy_Vacation_Map is shown below.


I utilize Google Directions API to create a route between Hervey Bay, Flinders, Bendigo, and Esperance, four arbitrary cities in Australia that are within the user's temperature preference. The route starts and stops in Hervey Bay and the travel mode is chosen to be bicycling. Lastly I added pop-up markers for each location that provides hotel name, city, country, current weather description, and maximum temperature. 

A screenshot of WeatherPy_Travel_Map_Markers is shown below.

