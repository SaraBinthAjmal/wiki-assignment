# wiki-assignment
# Wikipedia-like API – Productionized with Kubernetes & Helm

## Overview

This project productionizes a simplified Wikipedia-like API service that allows users to create users and posts. The service is built using ""FastAPI"" and has been containerized and deployed on ""Kubernetes"" using ""Helm"". The system is designed to be lightweight, observable, and production-ready within constrained resources.

The application exposes Prometheus metrics to track the total number of users and posts created, which are visualized using Grafana dashboards.

---

## Key Features

- Dockerized FastAPI application
- PostgreSQL-backed persistence layer
- Prometheus metrics collection
- Grafana dashboard for observability
- Kubernetes Ingress for unified access
- Configurable Docker image via Helm values
- Resource usage constrained to fit within:
  - 2 CPUs
  - 4GB RAM
  - 5GB disk

  ## Exposed Endpoints

### Application APIs
- `/users/*` → FastAPI service
- `/posts/*` → FastAPI service

### Grafana Dashboard
- `/grafana/d/creation-dashboard-678/creation`
- Username: `admin`
- Password: `admin`

---

## Metrics

The following Prometheus metrics are exposed by the FastAPI service

- `users_created_total` – Total number of users created
- `posts_created_total` – Total number of posts created

These metrics are visualized in Grafana using rate calculations over time.

---