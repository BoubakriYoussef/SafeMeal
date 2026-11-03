# SafeMeal

[![CI](https://github.com/BoubakriYoussef/repas_sur2/actions/workflows/ci.yml/badge.svg)](https://github.com/BoubakriYoussef/repas_sur2/actions/workflows/ci.yml)

SafeMeal is a full-stack web application designed for institutional and collective catering services. It centralizes diner profiles, food allergies, dietary requirements, dishes, menus, and meal services to minimize allergen-related risks during meal preparation and service.

## Project Overview

This repository contains the source code of a project developed as part of the French **RNCP Level 7 "Software Development Expert" certification**.

The project aims to demonstrate the design, development, testing, security, and deployment of a complete software solution addressing a real-world business challenge.

Its main objectives are to:

- Ensure reliable management of sensitive food allergy information.
- Support catering teams in meal planning and preparation.
- Proactively identify potential allergen-related risks.
- Track risk alerts and corrective actions.
- Improve operational safety through structured data management and automated risk detection.

## Business Problem

In institutional catering environments, managing diverse dietary profiles, food allergies, and operational constraints increases the risk of human error.

RepasSur addresses this challenge by providing a centralized platform that structures business data and automatically identifies incompatibilities between diners, dishes, and menus.

The application helps catering teams anticipate potentially hazardous situations and manage corrective actions.

## Key Features

- Secure JWT-based authentication and role-based access control (RBAC).
- Diner profile and dietary restriction management.
- Allergen and dietary requirement management.
- Catering site management.
- Dish, menu, and meal service management.
- Automated allergen risk assessment.
- Risk alert tracking and corrective action management.
- RESTful API documentation using OpenAPI / Swagger.
- Application monitoring through Spring Boot Actuator and Prometheus.

## Technology Stack

| Category | Technologies |
|---|---|
| Backend | Java 21, Spring Boot, Spring Security, Spring Data JPA, Hibernate, Liquibase |
| Frontend | Angular 20 |
| Database | PostgreSQL 15 |
| Containerization | Docker, Docker Compose |
| Backend Testing | JUnit 5, Spring Test, Mockito |
| Frontend Testing | Karma, Jasmine |
| CI/CD | GitHub Actions |
| Code Coverage | JaCoCo |
| Monitoring & Observability | Spring Boot Actuator, Prometheus, Grafana, Alertmanager, Blackbox Exporter |

## System Architecture

RepasSur follows a **three-tier architecture**, consisting of:

1. **Presentation Layer:** An Angular frontend providing the user interface.
2. **Application Layer:** A Spring Boot backend exposing RESTful APIs and implementing business logic.
3. **Data Layer:** A PostgreSQL database ensuring persistent storage of application data.

The application is structured around the following core business entities:

- Diner (`Convive`)
- Allergen (`Allergene`)
- Dietary Requirement (`Regime`)
- Dish (`Plat`)
- Menu (`Menu`)
- Meal Service (`ServiceRepas`)
- Risk Alert (`AlerteRisque`)
- Corrective Action (`ActionCorrective`)
- Catering Site (`SiteRestauration`)
- User (`Utilisateur`)

### Architecture Diagram

![System Architecture](docs/images/architecture.png)

### Simplified UML Class Diagram

![UML Class Diagram](docs/images/uml-classes.png)

## Repository Structure

```text
repas_sur2/
├── backend/repas_sur_backend2      # Spring Boot REST API
├── frontend/repas_sur_frontend2    # Angular application
├── monitoring/                     # Prometheus configuration
├── docs/images/                    # Architecture and UML diagrams
├── docker-compose.yml              # Complete local environment
├── DEPLOYMENT.md                   # VPS deployment guide
└── README-MIGRATIONS.md            # Database migration documentation
```

## Prerequisites

### Docker-Based Deployment

- Docker
- Docker Compose

### Local Development

- Java 21
- Maven Wrapper (included in the repository)
- Node.js and npm
- PostgreSQL 15

## Environment Configuration

The project provides an [`.env.example`](.
