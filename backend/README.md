# CV Builder Backend

Spring Boot backend for the CV Builder application.

This is a standalone backend repository. The frontend is in a separate repository.

## Prerequisites

- Java 17 or higher
- Maven 3.6 or higher

## Setup

1. Clone this repository:
```bash
git clone <backend-repository-url>
cd <backend-repository-name>
```

2. Build the project:
```bash
mvn clean install
```

3. Run the application:
```bash
mvn spring-boot:run
```

The backend will start on `http://localhost:8080`

## API Endpoints

- `POST /api/resumes` - Create a new resume
- `GET /api/resumes/{id}` - Get a resume by ID
- `GET /api/resumes` - Get all resumes
- `PUT /api/resumes/{id}` - Update a resume
- `DELETE /api/resumes/{id}` - Delete a resume

## Database

By default, the application uses H2 in-memory database for development. 
Access the H2 console at: `http://localhost:8080/h2-console`

For production, configure PostgreSQL in `application.properties`.

## CORS

CORS is configured to allow requests from `http://localhost:4200` (Angular frontend).

To allow requests from a different origin, update `src/main/resources/application.properties`:

```properties
spring.web.cors.allowed-origins=http://localhost:4200,http://your-frontend-url
```

Or modify the CORS configuration in `src/main/java/com/cvbuilder/config/CorsConfig.java`.

