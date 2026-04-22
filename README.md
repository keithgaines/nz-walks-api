# New Zealand Walks API — ASP.NET Core REST API

RESTful API built with ASP.NET Core for managing walking trail data across New Zealand, with authentication, role-based authorization, and full CRUD support for regions and walks.

---

## Overview

This API provides structured access to walking trail data across New Zealand, supporting both read and administrative operations.

It demonstrates:
- RESTful API design using ASP.NET Core
- Clean separation of concerns (controllers, services, data layer)
- JWT-based authentication and role-based access control
- Query support for filtering, sorting, and pagination
- Database-driven architecture using Entity Framework Core

---

## Core Features

- Region management (CRUD operations)
- Walk management with filtering and pagination
- Role-based access control (Reader / Writer)
- JWT authentication for protected endpoints
- Structured relational data model using SQL Server
- Scalable REST API architecture

---

## Technical Stack

- ASP.NET Core Web API  
- C#  
- Entity Framework Core  
- SQL Server  
- JWT Authentication  

---

## Architecture Overview

The system is structured using a layered API architecture:

- **Controllers** — Handle HTTP requests and route mapping  
- **Services Layer** — Encapsulates business logic  
- **Data Layer** — Entity Framework Core DbContext and persistence  
- **Models** — Domain entities and DTOs  

This structure supports separation of concerns and long-term extensibility.

---

## Authentication & Authorization

This API uses JWT (JSON Web Tokens) for authentication.

Two primary roles are enforced:
- **Reader** — Read-only access to resources  
- **Writer** — Full access to create, update, and delete resources  

Authenticated requests must include:
```
Authorization: Bearer <token>
```

---

## Endpoints

### Regions

- `GET /api/regions` — Retrieve all regions  
- `GET /api/regions/{id}` — Retrieve a specific region  
- `POST /api/regions` — Create region (Writer only)  
- `PUT /api/regions/{id}` — Update region (Writer only)  
- `DELETE /api/regions/{id}` — Delete region (Writer only)  

---

### Walks

- `GET /api/walks` — Retrieve walks (supports filtering, sorting, pagination)  
- `GET /api/walks/{id}` — Retrieve a specific walk  
- `POST /api/walks` — Create walk (Writer only)  
- `PUT /api/walks/{id}` — Update walk (Writer only)  
- `DELETE /api/walks/{id}` — Delete walk (Writer only)  

---

## Design Decisions

- Used JWT authentication to decouple identity from API logic  
- Implemented role-based authorization for secure write operations  
- Designed endpoints around resource-based REST principles  
- Added filtering/sorting/pagination to support scalable data access patterns  
- Separated concerns into service and controller layers for maintainability  

---

## What This Project Demonstrates

- REST API design using ASP.NET Core  
- Authentication and authorization with JWT  
- Clean architecture and separation of concerns  
- Backend data modeling with Entity Framework Core  
- Production-style API design patterns (filtering, pagination, role control)  

---

## Context

This project was built as a backend-focused exercise in designing secure, scalable REST APIs using ASP.NET Core and modern .NET practices.
