# Build a Weather Web App :sunny:

This week's project is to build a simple weather web app that shows today's weather and temperature, and a 5-day forecast using a weather API.

The web app, before stretch goals should look something along the lines of this:

![Design](https://github.com/Technigo/project-wheater-dash/blob/master/wireframe_weather.png)

We've asked a couple of different designers to do their take on this project. If you're not a designer yourself feel free to use their designs or simply be inspired by their solutions. It's also a great practice in implementing someone else's design. You will find their suggestions in the design folder in the repo along with some design assets.

---

## What you will learn 🧠

- What an API is and how to use it
- Basic JSON
- How to use `fetch()` in JavaScript
- How to use promises in JavaScript
- How to work with the `Date()` object in JavaScript

## How to get started 💪🏼

1. Fork this repo
2. Clone this repo into your projects folder on your computer
3. Open up VS Code and start coding!

### #1 Get started with the weather API.

[Sign up for a free Open Weather Map account](https://home.openweathermap.org/users/sign_up). Once signed in, go to the "Api Keys" tab and copy the API Key. You can use the API Key in the APPID parameter when making calls to the openweathermap API.

For example, to get the current weather in Stockholm, you can use the url below. Remember to replace "YOUR_API_KEY" with the API key you copied from your dashboard.

http://api.openweathermap.org/data/2.5/weather?q=Stockholm,Sweden&units=metric&APPID=YOUR_API_KEY


The response should look something like this (this has been run through jsonlint.com to add newlines and indentation):

```json

{
	"coord": {
		"lon": 18.06,
		"lat": 59.33
	},
	"weather": [{
		"id": 800,
		"main": "Clear",
		"description": "clear sky",
		"icon": "01d"
	}],
	"base": "stations",
	"main": {
		"temp": 6.47,
		"pressure": 1007,
		"humidity": 56,
		"temp_min": 6,
		"temp_max": 7
	},
	"visibility": 10000,
	"wind": {
		"speed": 3.6,
		"deg": 200
	},
	"clouds": {
		"all": 0
	},
	"dt": 1509709800,
	"sys": {
		"type": 1,
		"id": 5420,
		"message": 0.0024,
		"country": "SE",
		"sunrise": 1509689610,
		"sunset": 1509720490
	},
	"id": 2673730,
	"name": "Stockholm",
	"cod": 200
}
```

As you can see, there's a bunch of useful information in there - including current temperature, windspeed, humidity, etc.

You will need to use the `fetch()` function in JavaScript to load the weather data into your page, and then select the values you want to inject into the DOM from the JSON which comes from the API.

### #2 Present some data on your web app

Your task is to present the data: the city name, the temperature (rounded to 1 decimal place), and what type of weather it is (the "description" in the JSON)

### #3 Sunrise and sunset 🌇

Show the time for sunrise and sunset in a readable time format (Example: 13:00 or 1 PM). 
You will have to format the date from milliseconds to a readble format.

[Here](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date) is a useful resource for how to do this.

### #4 Weather forecast

Show a forecast for the next 5 days. You can choose how to display the forecast - perhaps you want to show the min and max temperature for each day, or perhaps you want to show the temperature from the middle of the day. Take a look at the api response from the [5 day forecast endpoint](https://openweathermap.org/forecast5) and decide how you'd like to format your data.

For example, you could use this query to get the next 5 days forecast for Stockholm:

http://api.openweathermap.org/data/2.5/forecast?q=Stockholm,Sweden&units=metric&APPID=YOUR_API_KEY

Here you can change city and amount of days.

*Parameters:*
**q** city name and country code divided by comma, use ISO 3166 country codes

Read the [endpoint documentation](https://openweathermap.org/forecast5) for more parameters you can pass.

If you take the url above (http://api.openweathermap.org/data/2.5/forecast?q=Stockholm,Sweden&units=metric&APPID=YOUR_API_KEY) and replace `YOUR_API_KEY` with the api key you copied and open the url in the browser, you can take a look at the data. You can install a [JSON formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa) chrome extension to make it easier to view.

### #5 Style your weather app 🎨

Once you get the data onto your site, style it to look like ine of the provided designs.

## Requirements 🧪

- You should fetch data from the API using `fetch()` in JavaScript 
- All data in the sketch above should be present and fetched from the API
- The presentation of the data should be in the specified format. 
- The page should work on mobile (mobile first!), tablet and desktop (Be responsive)
- Code follows Technigo’s code guidelines.
- Contribute by helping others with this project on Stack Overflow.
- If selected; demo your solution for your team.

## How to hand in the code 🎯

- When you’re finished with the project, push your code to GitHub with these commands:

  ```
  git add .
  git commit -m "your commit message"
  git push origin master
  ```

- Navigate to your repo and create a Pull Request into the Technigo repo (Add a link to your deployed project.)
- Wait for the code review from your teachers

## How to get help 🆘

Ask for help and share your knowledge about this project with the 'weather-app' tag on [Stack Overflow](https://stackoverflow.com/c/technigo/questions). Talk to your team on Slack and help each other out. Do some research about your problem, you are surely not the first one with this problem, Google is your friend 🙂. And you can of course also book a tech call. 

## Stretch Goals 🏃‍♂

Make sure you've commited and pushed a version of your project before starting with the stretch goals.

**_Design_**

Change the colors of the page based on the weather. If the weather is warm – use warm colors. If the weather is colder, use cold colors. If you really want to push you CSS muscles you can even make a [background gradient.](https://www.w3schools.com/css/css3_gradients.asp) 

**_Deep-dive_**

***Use your location***

Use the [Geolocation API](https://www.w3schools.com/html/html5_geolocation.asp) that is built in to your browser to fetch the city that you are located in atm and show the weather for your location. 

***Add multiple cities***

Give the user the option to choose between a couple of your favourite cities. 

#### 🚨 Don't forget to add, commit and push the changes to GitHub when you're done. 🏁
