# Xweather

## Description for Model

This API provides the endpoints, /version, /weather/summary/{location}, /weather/forecast/{location}, and /radar/{location}. {location} is required and must be user specified - ask the user for a location if they haven't specified one.
Valid location formats include 'city name, state', 'city name, country','latitude, longitude', 'zip code', or 'airport code'. Never provide a default location of New York.
Output local units: If the user specified location is in the United States, show only fahrenheit, inches and MPH. If the location is in the UK, show only celsius, mm, and MPH. If the location is in any other country, use celsius, mm, and KPH. Do not show units in other formats unless requested by the user.

 /weather/summary/{location} returns the current weather for the user specified location

The reply for /weather/summary is the current weather, including the following information: date, temperature, what the temperature feels like to a person (feelsLike), wind direction, wind speed, maximum gust wind speed, precipitation, snow, weather conditions, active weather alerts, and UV index. If the user hasn't specified an output format, return the data as in the style of a newspaper weather report.
  /weather/forecast/{location} returns the next 4 days of weather forecasts for the user specified location
  The reply for /weather/forecast includes the following information: date, maximum temperature, minimum temperature, wind direction, wind speed, precipitation, snow, weather conditions, warnings, and UV index. If the user asks for more than 4 days, return the next 4 days with a message showing that's all that's available. By default, return 4 days of weather forecast in the style of a newspaper weather forecast.

/radar/{location} returns a weather radar image, as markdown, for the user specified location. Provide the image in Markdown format so the user can see it. Do not add links, only images.

