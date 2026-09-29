# Weather Integration
Simple weather integration made with camel karavan, which receives a POST request with name and city, and returns the current temperature at the specified location. 
Uses [Open-Meteo](https://open-meteo.com) Geocoding and Forecast APIs to get the location and weather data.

## Prerequisites

Tools needed to build and deploy the application locally:

- Docker Desktop
- Minikube
- kubectl
- Java
- Git

## Integration

Integration is called with a 'POST /weather' request with a body for example:
{
    "name": "Juho",
    "city": "Turku"
}

And it responds with current time and current temperature at the specified city added:
{
  "name": "Juho",
  "city": "Turku",
  "currentTemperature": 16.7,
  "time": "2026-09-28T14:48:46Z"
}

Example request:
```
curl -X POST http://127.0.0.1:57285/weather -H "Content-Type: application/json" -d "{\"name\":\"Juho\",\"city\":\"Turku\"}"
```

### Made By
Juho Ollila