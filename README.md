## Functionality

This Flask application serves basic informational routes for a car company's model catalog.

### Routes

**`GET /`**
Returns a welcome message introducing the company.

Response: `Welcome to Flatiron Cars`

**`GET /<model>`**
Accepts a car model name as a URL parameter and checks it against the company's list of existing models (`existing_models`).

- If the model exists in the fleet, returns a confirmation message:
  `Flatiron {model} is in our fleet!`
  (e.g. `GET /Crossroads` → `Flatiron Crossroads is in our fleet!`)

- If the model does not exist in the fleet, returns a not-found message:
  `No models called {model} exists in our catalog`
  (e.g. `GET /realCar` → `No models called realCar exists in our catalog`)

### Current fleet

The app currently recognizes the following models: `Beedle`, `Crossroads`, `M2`, `Panique`.

### Running locally

```bash
cd server
pipenv install
pipenv run python app.py
```

The server runs on `http://localhost:5555`.

### Testing

```bash
cd server
pipenv run pytest
```

![App running]