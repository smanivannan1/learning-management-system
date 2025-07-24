# Student Course Management System

I designed and developed a full-stack web-based application that simulates key workflows of modern online learning systems, supporting both student and instructor access. Students can register, browse and enroll in available courses, submit course-specific assignments, and view grades for individual submissions and cumulative course performance. Instructors have a dedicated interface to view and manage student enrollment, create and update courses/content, post assignments, grade submissions, and manage students across multiple classes. The system automatically calculates and updates each student’s course grade by aggregating assignment scores, allowing students to view their performance across all enrolled courses in a centralized dashboard. I implemented secure role-based access in a microservices architecture, and designed a multi-page frontend webpage for personalized, user-specific content. I designed and populated the platform with real courses and layouts inspired by my university for demo purposes, and I hosted the application on the cloud so users can use it reliably without needing to install anything.

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

- **Inter-Service Communication**: Independent microservices communicate via REST (using Feign clients)
- **User Service** – Handles user registration, login, role assignment, and JWT for secure authentication
- **Course Service** – Manages course data (CRUD operations, search)  
- **Enrollment Service** – Handles student course enrollments and status (ACTIVE vs INACTIVE)
- **Assignment Service** – Enables instructors to create assignments and students to view assigned work and due dates
- **Submission Service** – Handles student assignment submissions and feedback from the instructor side
- **Gradebook Service** – Calculates overall grades for students based on assignment scores and exposes grade data per course and student
- **API Gateway & Service Discovery**: Routes traffic using Spring Cloud Gateway with dynamic service registration via Eureka
- **Containerization**: All services are containerized with Docker for isolated, scalable deployment, 


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

