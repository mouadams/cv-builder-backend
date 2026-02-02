CV Builder Backend

Spring Boot backend for the CV Builder application – a platform to create, manage, and download professional resumes online. This backend exposes REST APIs for handling users, resumes, and templates, and connects seamlessly with an Angular frontend.

Features

User authentication and management

CRUD operations for resumes (personal info, education, experience, skills)

Multiple resume templates support

RESTful API for frontend integration

Validation and error handling

Configurable database (H2 for development, PostgreSQL/MySQL for production)

CORS configured for Angular frontend

Prerequisites

Java 17 or higher

Maven 3.6 or higher

Setup

Navigate to the backend directory:

cd backend


Build the project:

mvn clean install


Run the application:

mvn spring-boot:run


The backend will start on: http://localhost:8080

API Endpoints

POST /api/resumes – Create a new resume

GET /api/resumes/{id} – Get a resume by ID

GET /api/resumes – Get all resumes

PUT /api/resumes/{id} – Update a resume

DELETE /api/resumes/{id} – Delete a resume

Database

Development: H2 in-memory database
Access H2 console: http://localhost:8080/h2-console

Production: Configure PostgreSQL or MySQL in application.properties

CORS

Configured to allow requests from the Angular frontend running at http://localhost:4200.

Technologies Used

Backend: Spring Boot, Java

Database: H2 (development), PostgreSQL/MySQL (production)

Security: Spring Security (optional JWT integration)

ORM: Hibernate / Spring Data JPA

Build Tool: Maven

Testing: Postman / Swagger (optional)

Contributing

Feel free to fork this repository, make improvements, and submit a pull request.
