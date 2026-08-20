# Microservices Config Repo

This repository contains centralized configuration files for microservices in the application architecture.

## Overview

This config-repo is designed to work with Spring Cloud Config Server to provide externalized configuration for microservices. Each service has its own configuration file that defines properties like database connections, server ports, logging levels, and service discovery settings.

## Configured Services

### Student Service
- **File**: `student-service.yml`
- **Application Name**: student-service
- **Server Port**: 8081
- **Database**: MySQL (localhost:3306/ritesh_db)
- **Logging Level**: DEBUG
- **Dependencies**:
  - Address Service: http://localhost:8082
- **Service Discovery**: Eureka (http://localhost:8761/eureka)

## Configuration Structure

Each service configuration file typically includes:

- **Logging**: Application logging levels
- **Spring**: Application name and datasource configuration
- **Server**: Port configuration
- **Service**: Inter-service communication URLs
- **Eureka**: Service discovery client configuration

## Usage

1. Set up a Spring Cloud Config Server pointing to this repository
2. Configure each microservice to fetch configuration from the config server
3. Services will automatically load their respective configuration files based on their application name

## Prerequisites

- Spring Cloud Config Server
- MySQL database (for services requiring database connectivity)
- Eureka Server (for service discovery)
- Network connectivity between services

## Service Ports

- Student Service: 8081
- Address Service: 8082
- Eureka Server: 8761