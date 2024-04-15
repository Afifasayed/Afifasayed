import requests
import json
import data
from typing import Union

def get_weather(city_name: str, api_key: str) -> None:

# Base URL from OpenWeatherMap.
    base_url = "http://api.openweathermap.org/data/2.5/weather?"

# Complete URL for fetching weather info: f"(base_url)q=(city_name)&appid=(api_key)" / Fill city name and api key.
    complete_url = f"http://api.openweathermap.org/data/2.5/weather?q=India&appid=5056c44a77f40026c9c833ec7a211060"

# Paste the request.get URL in Postman for getting the weather info for a specific city.
    response = requests.get('http://api.openweathermap.org/data/2.5/weather?q=India&appid=5056c44a77f40026c9c833ec7a211060')

# Example pretty-printed JSON data taken from Postman.
pretty_json_data = {
    "coord": {
        "lon": 12.2797,
        "lat": 46.7406
    },
    "weather": [
        {
            "id": 804,
            "main": "Clouds",
            "description": "overcast clouds",
            "icon": "04d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 285.15,
        "feels_like": 284.02,
        "temp_min": 285.15,
        "temp_max": 285.15,
        "pressure": 1018,
        "humidity": 62
    },
    "visibility": 10000,
    "wind": {
        "speed": 2.06,
        "deg": 300
    },
    "clouds": {
        "all": 100
    },
    "dt": 1712655949,
    "sys": {
        "type": 1,
        "id": 6809,
        "country": "IT",
        "sunrise": 1712637243,
        "sunset": 1712685016
    },
    "timezone": 7200,
    "id": 3168508,
    "name": "Innichen",
    "cod": 200
}

# Parse the JSON data into a Python Dictionary.
parsed_data: dict[int, any] = str({
    "coord": {
        "lon": 12.2797,
        "lat": 46.7406
    },
    "weather": [
        {
            "id": 804,
            "main": "Clouds",
            "description": "overcast clouds",
            "icon": "04d"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 285.15,
        "feels_like": 284.02,
        "temp_min": 285.15,
        "temp_max": 285.15,
        "pressure": 1018,
        "humidity": 62
    },
    "visibility": 10000,
    "wind": {
        "speed": 2.06,
        "deg": 300
    },
    "clouds": {
        "all": 100
    },
    "dt": 1712655949,
    "sys": {
        "type": 1,
        "id": 6809,
        "country": "IT",
        "sunrise": 1712637243,
        "sunset": 1712685016
    },
    "timezone": 7200,
    "id": 3168508,
    "name": "Innichen",
    "cod": 200
})

# Write city name for which you need weather info.
print("city: India")

# Assuming parsed_data is a dictionary
if isinstance(parsed_data, dict):
# Verify data type
    print("Data type:", type(parsed_data))

# Inspect dictionary keys
    print("Dictionary keys:", parsed_data.keys())

# Access the "deg" key if it exists.
if "deg" in parsed_data:
    print("deg:", ["300"])
else:
    print("parsed_data is not a dictionary")


# Access and work with a parsed data.
print(type(parsed_data))

# Print the parsed_data dictionary to inspect its structure
print(parsed_data)

if isinstance(data, dict) and "cod" in data:
  if data["cod"] != "404":
    get_weather()

# Type the weather info from Postman.
    weather_description = data[{
        "id": 800,
        "main": "Clear",
        "description": "clear sky",
        "icon": "01d"
    }]
    [0], ["clear sky"],
    wind_speed = data[{
        "speed": 1.54,
        "deg": 0
    }]
    ["1.54"],
    country = data[{
        "type": 1,
        "id": 6809,
        "country": "IT",
        "sunrise": 1712378389,
        "sunset": 1712425571
    }]["IT"],


temperature: Union[float, None] = 'weather_info', ["283.15"],
humidity: int = 'weather_info', ["71%"],
pressure: int = 'weather_info', ["1026 hPa"],
feels_like: Union[float, None] = 'weather_info', ["282.76, Kelvin"],

print(f"Weather Information for India:")
print(f"Temperature: 283.15 Kelvin ({283.15 - 273.15} Celsius)")
print(f"Humidity: 71%")
print(f"Pressure: 1026 hPa")
print(f"Feels Like: 282.76 Kelvin ({282.76 - 273.15} Celsius)")
print(f"Weather Description: clear sky")
print(f"Wind Speed: 1.54 m/s")
print("Feels like: 284.02")
print(f"Weather Description: Clear Sky")
print(f"Wind Speed: 1.54 m/s")




if __name__ == "__main__":

    city_name = "India"
    api_key = '5056c44a77f40026c9c833ec7a211060'
    get_weather('India', '5056c44a77f40026c9c833ec7a211060')
