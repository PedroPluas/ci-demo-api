# ci-demo-api

[![CI Pipeline](https://github.com/PedroPluas/ci-demo-api/actions/workflows/ci.yml/badge.svg)](https://github.com/PedroPluas/ci-demo-api/actions/workflows/ci.yml)

Small Spring Boot project built to demonstrate a professional Continuous Integration workflow using GitHub Actions.

## Project Goal

This project was built to practice CI fundamentals in a real workflow:

- build automation
- automated tests
- validation on every push
- visible execution evidence in GitHub Actions

## Tech Stack

- Java 21
- Spring Boot
- Maven
- JUnit 5
- GitHub Actions

## Available Endpoint

```bash
GET /api/v1/health
```

Example response:

```json
{
  "success": true,
  "message": "Application is running"
}
```

## Run Locally

```bash
./mvnw spring-boot:run
```

## Run Tests

```bash
./mvnw clean test
```

## Full Validation

```bash
./mvnw clean verify
```

## CI Workflow

The CI pipeline runs automatically on:

- push to `main`
- push to `develop`
- pull requests to `main` and `develop`

It performs the following steps:

- compile the application
- execute automated tests
- validate the project with Maven verify
- 
## Project Structure

```text
src/main/java
src/test/java
.github/workflows/ci.yml
```


