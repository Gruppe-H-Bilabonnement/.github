# Gruppe-H-Bilabonnement

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Flask](https://img.shields.io/badge/flask-%23000.svg?style=for-the-badge&logo=flask&logoColor=white)
![SQLite](https://img.shields.io/badge/sqlite-%2307405e.svg?style=for-the-badge&logo=sqlite&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![JWT](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white)
![Azure](https://img.shields.io/badge/Microsoft%20Azure-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)

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
   - Handles operations for car inventory.

3. **RentalService API**:
   - Manages rental contracts and their lifecycle.

4. **Damage Management API**:
   - Records and updates vehicle damage reports.

---

## Documentation

### JSON documentation
- API Gateway: `group-h-api-gateway-h9g7egage5a7dmd8.northeurope-01.azurewebsites.net/api/v1/`
- Car Management: `group-h-car-management-service-fhaeddg8agfddvdu.northeurope-01.azurewebsites.net/api/v1/`
- RentalService: `group-h-rental-service-emdqb2fjdzh7ddg2.northeurope-01.azurewebsites.net/api/v1/`
- Damage Management: `group-h-damage-management-service-ejh4byctd4hvh9dr.northeurope-01.azurewebsites.net/api/v1/`
### Swagger UI Endpoints
- API Gateway: `group-h-api-gateway-h9g7egage5a7dmd8.northeurope-01.azurewebsites.net/api/v1/docs`
- Car Management: `group-h-car-management-service-fhaeddg8agfddvdu.northeurope-01.azurewebsites.net/api/v1/docs`
- RentalService: `group-h-rental-service-emdqb2fjdzh7ddg2.northeurope-01.azurewebsites.net/api/v1/docs`
- Damage Management: `group-h-damage-management-service-ejh4byctd4hvh9dr.northeurope-01.azurewebsites.net/api/v1/docs`

---
