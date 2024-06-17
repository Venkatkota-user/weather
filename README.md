import requests
import sys

def get weather (api key, location):
        base_url="http://api.openweathermap.org/data/2.5/weather"
        params = {
                 "q": location,
                 "appid": api_key,
                 "units": "metric"
          }
          response = requests.get(base url, params-params)
          weather_data response.json()
          return weather data
def main():
        if len(sys.argv) < 2:
             print("Usage: python weather_python_code.py <city_name>") 
              return
        city_name = '.join(sys.argv[1:])
        api key=5be038eb38891439dee6768eala5d994
        try:
              weather_data = get_weather (api_key, city_name)
               if weather_data['cod'] != 200:
                       print("Error: (weather_data['message']}")
                       return
	weather = weather data['weather'] [0]
	main = weather data['main']
	wind = weather data['wind']

	print (f"Weather in (city_name): (weather ['description'])")
	print (f"Temperature: (main ['temp']) "C")
	print(f"Humidity: (main ['humidity']}%")
	print (f"Wind: (wind['speed']} m/s, {wind['deg'}}"")
         except Exception as e:
	    print (f"Error fetching weather data: (str(e)}")
if __name__ == "__main__":
       main()
