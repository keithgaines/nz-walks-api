# New Zealand Walks API

REST API built with ASP.NET Core for managing walking trail data across New Zealand.

The application provides secure access to regions and walks through JWT authentication, role-based authorization, and resource-based endpoints.

---

## Architecture

<img width="1536" height="1024" alt="APIArchImage" src="https://github.com/user-attachments/assets/d93785ed-bd79-4a13-b90f-5a9be15c9721" />


---

## Overview

This API provides structured access to walking trail data while demonstrating common backend patterns used in modern .NET applications.

The project focuses on:

* REST API design
* Authentication and authorization
* Layered architecture
* Database-driven applications
* Scalable query patterns

---

## Features

### Region Management

* Create regions
* Retrieve regions
* Update regions
* Delete regions

### Walk Management

* Create walks
* Retrieve walks
* Update walks
* Delete walks
* Filtering
* Sorting
* Pagination

### Security

* JWT authentication
* Role-based authorization
* Reader and Writer roles

---

## Technology Stack

### Backend

* ASP.NET Core Web API
* C#
* Entity Framework Core
* SQL Server

### Security

* JWT Authentication
* Role-based Access Control

---

## Authentication

Protected endpoints require a JWT token.

```http
Authorization: Bearer <token>
```

Two roles are supported:

### Reader

Read-only access.

### Writer

Create, update, and delete access.

---

## API Endpoints

### Regions

```http
GET     /api/regions
GET     /api/regions/{id}
POST    /api/regions
PUT     /api/regions/{id}
DELETE  /api/regions/{id}
```

### Walks

```http
GET     /api/walks
GET     /api/walks/{id}
POST    /api/walks
PUT     /api/walks/{id}
DELETE  /api/walks/{id}
```

Supports:

* Filtering
* Sorting
* Pagination

---

## Design Decisions

* Used JWT authentication to separate identity from API logic
* Implemented role-based authorization for protected operations
* Designed endpoints around REST principles
* Added filtering and pagination for scalable queries
* Separated concerns into controller, service, and persistence layers

---

## What This Project Demonstrates

* REST API development with ASP.NET Core
* JWT authentication and authorization
* Layered architecture
* Entity Framework Core
* Database modeling
* Resource-based API design
* Filtering and pagination patterns

---

## Future Enhancements

* Swagger examples
* API versioning
* Request validation
* Structured logging
* Docker support
* Automated testing

---

## Repository

[https://github.com/keithgaines/NZWalksAPI](https://github.com/keithgaines/nz-walks-api)
