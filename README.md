# Student Course Management System

## Author

**Sachin Manivannan**  

---
I developed a full-stack web-based application that simulates key workflows of modern online learning systems, supporting both student and instructor access. Students can register, browse and enroll in available courses, submit course-specific assignments, and view grades for individual submissions and cumulative course performance. Instructors have a dedicated interface to view and manage student enrollment, create and update courses/content, post assignments, grade submissions, and manage students across multiple classes. The system automatically calculates and updates each student’s course grade by aggregating assignment scores, allowing students to view their performance across all enrolled courses in a centralized dashboard. I implemented secure role-based access in a microservices architecture, and designed a multi-page frontend webpage for personalized, user-specific content. I designed and populated the platform with real courses and layouts inspired by my university for demo purposes, and I hosted the application on the cloud so users can use it reliably without needing to install anything.

You can test out the platform here:

**Live Demo**: [http://34.173.28.213:4200/login](http://34.173.28.213:4200/login)
---
## Features

- **User Authentication**: JWT-based login system with secure registration and role-based access for students and instructors
- **Course Management**: Instructors can create, update, delete, and manage courses
- **Course Enrollment**: Students can browse courses and enroll or unenroll
- **Role-Based Access Control**: Separate access flows, dashboard, and permissions for students and instructors
- **Assignment Submission & Grading**: Students can submit assignments, and instructors can view, grade, and provide feedback
- **API Gateway & Service Discovery**: Routes traffic using Spring Cloud Gateway with dynamic service registration via Eureka

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

- **Inter-Service Communication**: Independent microservices communicate via REST using Feign clients
- **User Service** – Handles user registration, login, and role assignment using JWT for secure authentication
- **Course Service** – Manages course data, search functionality, and CRUD operations  
- **Enrollment Service** – Handles student enrollment using data retrieved from the User and Course services
- **Assignment Service** – Enables instructors to create assignments and students to view assigned work and due dates
- **Submission Service** – Handles student assignment submissions and scores/feedback from the instructor side
- **Gradebook Service** – Calculates overall grades for students based on submission scores and exposes grade data per course and student
- **Discovery Service** - Allows microservices to register themselves with Eureka so they can be dynamically discovered by other services
- **API Gateway Service**: Routes traffic to the appropriate service by acting as a centralized entry point for all client requests (via Spring Cloud Gateway and Eureka)
- **Containerization**: Dockerized all services and used Docker Compose to orchestrate and deploy the application on Google Cloud Platform


## Future Improvements

- OAuth2 support and enhanced security
- Redis caching and performance optimization
- CI/CD with GitHub Actions or Jenkins
- Kubernetes deployment for orchestration
- UI/UX improvements and full mobile responsiveness

---


