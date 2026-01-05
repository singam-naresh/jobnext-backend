JobNext – Job Portal Backend
JobNext is a backend-only job portal application built using Java and Spring Boot.
The project focuses on REST API design, backend architecture, and database-driven workflows commonly used in real-world applications.
This project demonstrates how job seekers and employers interact through backend services without a frontend layer.
🛠 Tech Stack
Java 17
Spring Boot
Spring Data JPA (Hibernate)
MySQL
Maven
REST APIs
Postman (API testing)
🧱 Architecture
The application follows a layered architecture to ensure clean separation of concerns:
Controller – Handles HTTP requests and responses
Service – Contains business logic
Repository – Data access layer using Spring Data JPA
Entity – Database entity models
DTO – Request and response objects
Exception – Centralized exception handling using @ControllerAdvice
🚀 Getting Started
Prerequisites
Java 17
Maven
MySQL
Setup Instructions
1. Clone the repository
Copy code
Bash
git clone https://github.com/singam-naresh/jobnext-backend.git
cd jobnext-backend
2. Create MySQL Database
Create a database named jobnext (or any name you prefer).
3. Configure Database
Update application.properties:
Copy code
Properties
spring.datasource.url=jdbc:mysql://localhost:3306/jobnext
spring.datasource.username=your_username
spring.datasource.password=your_password

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
4. Build and Run the Application
Copy code
Bash
mvn clean install
mvn spring-boot:run
5. Test APIs
Use Postman or any REST client to test the APIs.
📦 Core Modules
User Module
Register users as JOB_SEEKER or EMPLOYER
View user details
Job Module
Employers can post jobs
View all available jobs
View jobs posted by a specific employer
Application Module
Job seekers can apply for jobs
Track application status
🔗 Entity Relationships
One Employer can post multiple Jobs
One Job can have multiple Applications
One Job Seeker can apply to multiple Jobs
📮 API Endpoints
Users
POST /users
GET /users/{id}
Jobs
POST /jobs
GET /jobs
GET /jobs/employer/{employerId}
Applications
POST /applications
GET /applications/user/{userId}
📌 Sample API Requests & Responses
Create User
POST /users
Request:
Copy code
Json
{
  "name": "Naresh",
  "email": "naresh@example.com",
  "role": "JOB_SEEKER"
}
Response:
Copy code
Json
{
  "id": 1,
  "name": "Naresh",
  "email": "naresh@example.com",
  "role": "JOB_SEEKER"
}
Create Job
POST /jobs
Request:
Copy code
Json
{
  "title": "Java Backend Developer",
  "description": "Spring Boot backend role",
  "location": "Bengaluru",
  "postedBy": 2
}
Response:
Copy code
Json
{
  "id": 10,
  "title": "Java Backend Developer",
  "location": "Bengaluru"
}
Apply for Job
POST /applications
Request:
Copy code
Json
{
  "jobId": 10,
  "applicantId": 1
}
Response:
Copy code
Json
{
  "applicationId": 101,
  "status": "APPLIED"
}
🎯 Purpose of This Project
Practice real-world backend development using Java and Spring Boot
Understand entity relationships and backend business logic
Build interview-ready REST API experience
Strengthen backend architecture fundamentals
🛣 Roadmap
Add authentication and authorization
Improve validation and error responses
Add unit tests using JUnit and Mockito
📌 Note
This is a backend-only project.
No frontend implementation is included.
