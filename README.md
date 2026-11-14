# IoT Device Health Monitor

A multi-service platform that collects telemetry from simulated IoT devices
and estimates their health using machine learning.

- **Hub (Java, Spring Boot):** central REST backend that handles device
  registration, telemetry ingestion, security, and coordination between services.
- **ML service (Python, FastAPI):** serves a scikit-learn model that predicts
  device health from telemetry (temperature, vibration).
- **IoT simulator (Python):** generates realistic telemetry from multiple
  devices, including gradual fault scenarios.
- **Database (PostgreSQL):** stores devices, measurement history, and health status.
- **Infrastructure (Docker, Docker Compose):** each component runs in its own
  container; the whole system starts with `docker compose up`.
