

# Microservices E-Commerce Application

This repository contains the source code for a **Microservices-based E-Commerce Application**. It is designed using **Spring Boot** and incorporates modern DevOps practices with **Prometheus** and **Grafana** for monitoring, and deployment using **Docker**.

## Overview

The application consists of the following microservices:

1. **API Gateway**: Manages external requests and routes them to appropriate microservices.
2. **Discovery Service**: Handles service registration and discovery using Netflix Eureka.
3. **Product Service**: Manages product-related operations (CRUD, listing).
4. **Inventory Service**: Tracks product availability.
5. **Notification Service**: Sends notifications to users (e.g., email, SMS).
6. **Order Service**: Handles order management, processing, and status updates.

The project is designed with **scalability**, **fault tolerance**, and **observability** in mind.

---

## Features

### Key Functionalities
- E-Commerce operations such as product management, inventory tracking, order placement, and notifications.
- Centralized API Gateway for routing and request handling.
- Service registration and discovery with Netflix Eureka.

### Monitoring
- Integrated with **Prometheus** for real-time metrics collection.
- Visualized metrics with **Grafana** dashboards.

### Deployment
- Containerized microservices using **Docker**.

---

## Architecture

The application follows a **Microservices Architecture** with the following key components:

- **API Gateway**: Routes traffic to microservices.
- **Eureka Discovery**: Keeps track of all running services.
- **Spring Boot Microservices**: 
  - **Product Service**: Manages product data.
  - **Inventory Service**: Monitors stock levels.
  - **Order Service**: Handles order lifecycle.
  - **Notification Service**: Sends notifications for updates and events.

- **Prometheus & Grafana**: Integrated monitoring solution for visual insights and alerting.

---

## Prerequisites

Ensure the following tools are installed:
- **Java 17**
- **Maven** (for building Spring Boot projects)
- **Docker** (for containerization)
- **Prometheus** and **Grafana**

---

## Installation and Setup

### Clone the Repository
```bash
git clone https://github.com/Ilyes-Kasdallah/Microservices-Application.git
cd Microservices-Application
```

### Build the Microservices
Navigate to each microservice directory and run:
```bash
mvn clean install
```

### Run Locally (Using Docker Compose)
A `docker-compose.yml` file is included for local deployment:
```bash
docker-compose up --build
```

---

## Monitoring Setup

### Prometheus
Prometheus scrapes metrics from the application. Configuration files are included in the `monitoring/prometheus/` directory.

1. Deploy Prometheus:
   ```bash
   docker-compose up -d prometheus
   ```

### Grafana
Grafana visualizes metrics from Prometheus. Dashboards for the application are pre-configured.

1. Deploy Grafana:
   ```bash
   docker-compose up -d grafana
   ```

Access Grafana UI and import the dashboards from `monitoring/grafana/dashboards/`.

---

## Directory Structure

```
Microservices-Application/
│
├── api-gateway/             # API Gateway service
├── discovery-service/       # Service registry (Eureka)
├── product-service/         # Product management service
├── inventory-service/       # Inventory tracking service
├── order-service/           # Order management service
├── notification-service/    # Notifications service
│
├── monitoring/              # Monitoring setup (Prometheus & Grafana)
│   ├── prometheus/
│   └── grafana/
│
├── docker-compose.yml       # Docker Compose setup
└── README.md                # Project documentation
```

---

## Contribution

Contributions are welcome! Please fork the repository and submit a pull request for any improvements.

---

## License

This project is licensed under the MIT License. See the [LICENSE](https://www.geeksforgeeks.org/java-spring-boot-microservices-example-step-by-step-guide/) file for more details.

---

## Contact

If you have any questions or feedback, feel free to reach out:

- **Author**: Ilyes Kasdallah
- **GitHub**: [Ilyes-Kasdallah](https://github.com/Ilyes-Kasdallah)

---
