# Student Course Management System

A full-stack web application built using **Java Spring Boot Microservices**, **PostgreSQL**, and an **Angular frontend**, simulating a modern learning platform. Students can register/login, enroll/search courses, submit assignments, and view grades. Instructors manage course content and track student progress. The system features secure role-based access, modular microservice architecture, and scalable deployment on the cloud.

👉 **Live Demo**: [http://34.173.28.213:4200/login](http://34.173.28.213:4200/login)
---
## Features

- **User Authentication**: JWT-based login system with secure registration and role assignment for students and instructors
- **Course Management**: Instructors can create, update, delete, and manage courses
- **Course Enrollment**: Students can browse courses and enroll or unenroll
- **Role-Based Access Control**: Separate access flows and permissions for students and instructors
- **Service Communication**: Microservices communicate via REST (using Feign clients)
- **API Gateway & Service Discovery**: Routes traffic using Spring Cloud Gateway with dynamic service registration via Eureka
- **Containerization**: All services are containerized with Docker for isolated, scalable deployment

---

## Tech Stack

### Backend:
- **Java 17**, **Spring Boot**
- **Spring Security**, **JWT**
- **Spring Cloud Gateway**, **Eureka Discovery**
- **Spring Data JPA**, **Feign Clients**
- **RabbitMQ** (used for asynchronous messaging)
- **PostgreSQL**

### Frontend:
- **Angular**  
- **RESTful API** integration for dynamic data rendering

### DevOps:
- **Docker** for containerization  
- **Postman** for API testing  
- Deployed to **Google Cloud Platform** via Compute Engine

---

## Microservices Overview

- **User Service** – Handles registration, login, and role assignment  
- **Course Service** – Manages course data (CRUD operations, search)  
- **Enrollment Service** – Handles student course enrollments and history  
- **Progress Service** – Tracks lesson/module completion and generates reports  
- *(Optional)* **Recommendation Service** – Suggests courses based on interests

---

## Future Improvements

- OAuth2 support and enhanced security
- Redis caching and performance optimization
- CI/CD with GitHub Actions or Jenkins
- Kubernetes deployment for orchestration
- UI/UX improvements and full mobile responsiveness

---

## Author

**Sachin Manivannan**  

---

