# Python API Analysis

## Background

Utilized Python requests, APIs, and JSON traversals to answer a fundamental question: "What's the weather like as we approach the equator?"

## Part I - WeatherPy

In this part, I created a Python script to visualize the weather of 500+ randomly chosen cities across the world of varying distance from the equator. 

First, I created a series of scatter plots to showcase the following relationships:

* Temperature (F) vs. Latitude
* Humidity (%) vs. Latitude
* Cloudiness (%) vs. Latitude
* Wind Speed (mph) vs. Latitude

After each plot, is a brief explanation of what the code is analyzing and an interpretation of this information.

Next, I ran linear regression on each relationship. This time, I separated the plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude):

* Northern Hemisphere - Temperature (F) vs. Latitude
* Southern Hemisphere - Temperature (F) vs. Latitude
* Northern Hemisphere - Humidity (%) vs. Latitude
* Southern Hemisphere - Humidity (%) vs. Latitude
* Northern Hemisphere - Cloudiness (%) vs. Latitude
* Southern Hemisphere - Cloudiness (%) vs. Latitude
* Northern Hemisphere - Wind Speed (mph) vs. Latitude
* Southern Hemisphere - Wind Speed (mph) vs. Latitude

After each plot, is a brief explanation of what the code is analyzing and an interpretation of this information.

The information of these randomly selected cities and their weather data can be found [here](code/WeatherPy/output_data/cities_weather.csv). All charts are saved as PNG's and can be viewed [here](code/WeatherPy/output_data).

### Part II - VacationPy

In the second part, I used jupyter-gmaps and the Google Places API to find cities within the 500+ randomly selected cities whose weather matched my ideal locations. Then I found the closest Hotel to this location, if available. To accomplish this, I did the follow:

* Created a heat map that displays the humidity for every city from Part I.

* Narrowed down the DataFrame to match my ideal weather conditions:

  * A max temperature lower than 85 degrees but higher than 65.

  * Wind speed less than 10 mph.

  * Cloudiness less than 10%.

  * Humidity lower than 50%

  * Dropped any rows that don't contain all four conditions. 

* Next, I used Google Places API to find the first hotel for each city located within 5000 meters of your coordinates.

* Then, I plotted the hotels on top of the humidity heatmap with each pin containing the **Hotel Name**, **City**, and **Country**.


