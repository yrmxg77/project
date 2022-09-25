# project
import json, requests

base_url = "https://api.openweathermap.org/data/2.5/weather"
appid = "99dd3a9554dc4d210b5d1c2f0ddd0fed"
city= "Los Angeles"

url = f"{base_url}?q={city}&units=imperial&APPID={appid}"
print(url)
print ()

response= requests.get(url)
unformated_data = response.json()

#print(unformted_data)

temp = unformated_data["main"]["temp"]
print(f"The current temp is: {temp}")

temp_max = unformated_data["main"]["temp_max"]
print(f"The max temp is: {temp_max}")
