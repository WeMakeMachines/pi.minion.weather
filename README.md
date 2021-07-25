_pinion - a small cog which engages the teeth of a larger wheel_

# pinion.weather 😈⛅

- a small weather microservice

## Features

- Uses OpenWeatherMap API v2.5
- Keeps a local cache of the response data
- Allows mixing of units as metric / imperial for speed and temperature

## Operation

### Routes

- `/now` - returns the weather now
- `/hourly` - returns the weather for the next 48 hours
- `/daily` - returns the forecast for the next 8 days

### Parameters

- `speed=` - can be either `metric` or `imperial`
- `temperature=` - can be either `metric` or `imperial`

### Cache

#### Disable caching

If you want to disable system file writes, add to the `.env` file `DISABLE_CACHING` set to `True`

#### Deleting cache

Cached files are written to `/cache`

To delete the cache, simply delete this folder

## Installation and Usage

1. Make sure you have met the following dependencies on your system:
   - python >= 3.9.5
   - python pip
   - python venv
   
   See the guide [Installing Python Dependencies on Linux](./INSTALLING_PYTHON_DEPENDENCIES.md)
   
2. Create a `.env` file from the `.env.example`
   
    `python3 -m venv ./venv/`

3. Activate the virtual environment
   
    `. venv/bin/activate`
   
4. Install the requirements
   
    `pip install -r requirements.txt`

### Deploying on Linux

Running the following script will setup **pinion.weather** as a systemd service on Linux

`./register-service.sh`

### Development on Linux

To test the server, run the following command within the virtual environment

`flask run --host=0.0.0.0`
