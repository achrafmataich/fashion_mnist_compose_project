# Fashion MNIST Compose Project

A modular, production-ready AI-powered web application for Fashion MNIST image classification. This monorepo uses Docker Compose and git submodules for clean separation of concerns and easy deployment.

## Architecture

- **ai_model/**: Python gRPC server serving a Fashion MNIST classifier
- **backend/**: Spring Boot web backend, connects to AI model via gRPC
- **frontend/**: Angular web app for user interaction
- **docker-compose.yml**: Orchestrates all services

## Quick Start

### Prerequisites
- Docker & Docker Compose
- Git

### Clone with Submodules
```bash
git clone --recurse-submodules https://github.com/achrafmataich/fashion_mnist_compose_project.git
```

### Start All Services

Before starting the services via compose, please create a file `environment.staging.ts` in `frontend/src/environments/` and set the values you have configured, this is the working values if you didn't change anything in the cloned repository:

```ts
export const environment = {
    apiUrl: "/api",
    predictEndpoint: "/prediction/predict/json"
};
```

Then run the compose project

```bash
docker-compose up --build
```

---

## References
- See submodule `README`s for more details

---

## Author

<img src="https://avatars.githubusercontent.com/u/100163733?size=128" alt="Achraf MATAICH" width="64" height="64" style="border-radius: 50%;">

[Achraf MATAICH](https://github.com/achrafmataich) <achraf.mataich@outlook.com>

