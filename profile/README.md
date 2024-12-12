# Gruppe-H-Bilabonnement

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)

A comprehensive and modular solution for managing a car subscription service, comprising multiple microservices and an API Gateway for seamless integration.

## Project Overview

Gruppe-H-Bilabonnement is a microservice-based architecture designed to manage the operations of a car subscription service efficiently. It consists of the following components:

1. **API Gateway**: Centralized entry point for all services.
2. **Car Management API**: Manages car inventory and details.
3. **RentalService API**: Handles rental contracts.
4. **Damage Management API**: Manages vehicle damage reports.

Each component is designed to operate independently while integrating smoothly through the API Gateway.

---

## Key Features

### Technical Highlights
- **Microservice Architecture**: Independent, scalable services for modular development.
- **Centralized Authentication**: Secure JWT-based authentication through the API Gateway.
- **RESTful Design**: Standardized and predictable endpoints.
- **Interactive Documentation**: Swagger UI for all services.
- **Cloud-Ready**: Deployed and tested on Azure.

### Functional Capabilities
- User registration and authentication.
- Manage car inventory, rental contracts, and damage reports.
- Centralized logging and error handling.
- Cross-service communication for efficient workflows.

---

## Architectural Design

### System Components

1. **API Gateway**:
   - Routes requests to the appropriate microservice.
   - Provides centralized authentication and documentation.

2. **Car Management API**:
   - Handles CRUD operations for car inventory.

3. **RentalService API**:
   - Manages rental contracts and their lifecycle.

4. **Damage Management API**:
   - Records and updates vehicle damage reports.

---

## 📂 Project Structure
```
Gruppe-H-Bilabonnement/
│
├── api-gateway-service/
│   ├── app.py                   # Main application entry point
│   ├── database/
│   │   └── initialize.py        # Database setup
│   ├── swagger/
│   │   ├── config.py            # Swagger configuration
│   │   └── docs/                # Swagger documentation specs
│   └── .env                     # Environment variables
│
├── car-management-service/
│   ├── app.py                   # Main application entry point
│   ├── database/
│   │   └── initialization.py    # Database setup
│   ├── swagger/
│   │   ├── config.py            # Swagger configuration
│   │   └── docs/                # Swagger documentation specs
│   └── xlsx/
│       └── Bilabonnement_2024_Clean.xlsx
│
├── rental-service-api/
│   ├── app.py                   # Main application entry point
│   ├── database/
│   │   ├── connection.py        # Database connection
│   │   └── initialization.py    # Database setup
│   ├── swagger/
│   │   ├── config.py            # Swagger configuration
│   │   └── docs/                # Swagger documentation specs
│   └── xlsx/
│       └── bilabonnement_2024_Clean.xlsx
│
├── damage-management-service/
│   ├── app.py                   # Main application entry point
│   ├── database/
│   │   └── initialization.py    # Database setup
│   ├── swagger/
│   │   ├── config.py            # Swagger configuration
│   │   └── docs/                # Swagger documentation specs
```

---

## Documentation

### Swagger UI Endpoints
- API Gateway: `/api/v1/docs`
- Car Management: `/api/v1/car-management/docs`
- RentalService: `/api/v1/rentals/docs`
- Damage Management: `/api/v1/damage-management/docs`

---

## Setup and Deployment

### Local Setup

```bash
# Set up virtual environments and dependencies for each service
cd api-gateway-service
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

cd ../car-management-service
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

cd ../rental-service-api
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt

cd ../damage-management-service
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

### Docker Deployment

```bash
# Build and deploy all services
cd api-gateway-service
docker build -t api_gateway_service .
docker run -d -p 80:80 --name api_gateway_container api_gateway_service

cd ../car-management-service
docker build -t car_management_service .
docker run -d -p 81:80 --name car_management_container car_management_service

cd ../rental-service-api
docker build -t rental_service .
docker run -d -p 82:80 --name rental_service_container rental_service

cd ../damage-management-service
docker build -t damage_management_service .
docker run -d -p 83:80 --name damage_management_container damage_management_service
```
