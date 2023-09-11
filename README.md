# Build-a-weather-application-that-fetches-weather-data-using-a-weather-API-e.g.-
import requests

def get_weather(city, api_key):
    url = f"https://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}"
    response = requests.get(url)
    data = response.json()
    return data

def main():
    city = input("Enter city name: ")
    api_key = "YOUR_API_KEY"  # Replace with your API key
    weather_data = get_weather(city, api_key)
    print(f"Weather in {city}: {weather_data['weather'][0]['description']}")

if __name__ == "__main__":
    main()
