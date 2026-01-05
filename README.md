# JobNext – Job Portal Backend

JobNext is a backend-only job portal application built using Java and Spring Boot.  
The project focuses on REST API design, backend architecture, and database-driven workflows commonly used in real-world applications.

This project demonstrates how job seekers and employers interact through backend services without a frontend layer.

---

## 🛠 Tech Stack
- Java 17
- Spring Boot
- Spring Data JPA (Hibernate)
- MySQL
- Maven
- REST APIs
- Postman (API testing)

---

## 🧱 Architecture
The application follows a layered architecture:

- Controller – Handles HTTP requests and responses
- Service – Contains business logic
- Repository – Data access layer using JPA
- Entity – Database entity models
- DTO – Request and response objects
- Exception – Centralized exception handling

---

## 📦 Core Modules

### User
- Register users as Job Seeker or Employer
- View user details

### Job
- Employers can post jobs
- View all available jobs
- View jobs posted by a specific employer

### Application
- Job seekers can apply for jobs
- Track application status

---

## 🔗 Entity Relationships
- One Employer can post multiple Jobs
- One Job can have multiple Applications
- One Job Seeker can apply to multiple Jobs

---

## 🚀 Key Features
- RESTful API design
- CRUD operations using Spring Data JPA
- MySQL relational database integration
- Input validation using annotations
- Centralized exception handling
- Clean separation of concerns

---

## 📮 Sample API Endpoints
- POST /users
- POST /jobs
- GET /jobs
- POST /applications
- GET /applications/user/{userId}

---

## 🎯 Purpose of This Project
- Practice real-world backend development using Java
- Understand entity relationships and business logic
- Build interview-ready backend experience

---

## 📌 Note
This is a backend-only project with no frontend implementation.
