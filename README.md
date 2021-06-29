# pinion.weather 😈⛅

_pinion - a small cog which engages the teeth of a larger wheel_

- a small weather microservice

## Dependencies

- Python 3.9.5
- faster_than_requests
- Flask
- python-dotenv

## Setup

1. Create a `.env` file from the `.env.example`
2. `. venv/bin/activate`
2. `flask run`

## Routes

- `/weather/now` - returns the weather now
- `/weather/hourly` - returns the weather for the next 48 hours
- `/weather/daily/{n}` - returns the forecast for the next {n} days. Up to 8.

## TODO

- Implement caching in OpenWeatherMap module
