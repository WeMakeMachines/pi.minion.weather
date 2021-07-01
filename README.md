_pinion - a small cog which engages the teeth of a larger wheel_

# pinion.weather 😈⛅

- a small weather microservice

## Features

- Uses OpenWeatherMap API
- caches response data

## Routes

- `/weather/now` - returns the weather now
- `/weather/hourly` - returns the weather for the next 48 hours
- `/weather/daily` - returns the forecast for the next 8 days

## Dependencies

- flask
- python-dotenv
- requests

## Setting up development (Linux)

### Setup Python 3

`sudo apt-get install python3 python-pip python3-venv`

### Setup

Create a `.env` file from the `.env.example`

```
python3 -m venv ./venv/
. venv/bin/activate
pip install -r requirements.txt
flask run --host=0.0.0.0
```
