# Deploy Test App

A .NET 9.0 Web API application for testing deployment workflows with Docker containerization.

## Summary

Simple ASP.NET Core Web API with WeatherForecast endpoint, built with .NET 9.0 and Docker support. Includes Swagger UI for API documentation.

## Requirements

- [.NET 9.0 SDK](https://dotnet.microsoft.com/download/dotnet/9.0) (for local development)
- [Docker](https://www.docker.com/get-started) (for containerized deployment)

## Build & Run

### Local Development
```bash
# Restore, build and run
dotnet restore
dotnet build
dotnet run

# Access at http://localhost:5173
# Swagger UI at http://localhost:5173/swagger
```

### Docker
```bash
# Build image
docker build -t deploy-test-app .

# Run container
docker run -d -p 8080:80 --name deploy-test-app-container deploy-test-app

# Access at http://localhost:8080
# Swagger UI at http://localhost:8080/swagger
```

## API

- **GET** `/WeatherForecast` - Returns weather forecast data

Example response:
```json
[
  {
    "date": "2025-09-11",
    "temperatureC": 31,
    "temperatureF": 87,
    "summary": "Scorching"
  }
]
```
