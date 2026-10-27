Customer Feedback Portal — Starter Kit

A responsive feedback form concept for Cloudsoftera, with conditional follow-up questions and a Spring Boot + MariaDB/MySQL persistence starter.

## Included
- `frontend/index.html` — responsive single-page feedback form, validation, conditional experience/support questions, service selector, accessible controls.
- `backend/` — Spring Boot REST API starter with JPA entity, repository, DTO, controller, and configuration.
- `database/schema.sql` — database/table creation.

## Run the frontend
Open `frontend/index.html` for a UI preview. To save submissions, run the backend and serve the frontend from an allowed origin (CORS is configured for localhost preview). Update the API URL in the HTML if needed.

## Run the backend
Use Java 21+ and Maven. Create the database first:
```sql
SOURCE database/schema.sql;
```
Then configure `backend/src/main/resources/application.properties` with your database credentials and run:
```bash
cd backend
mvn spring-boot:run
```
The API endpoint is `POST http://localhost:8080/api/feedback`.

## Important integration notes
- Before production, add authentication/authorization if feedback is internal, rate limiting, spam protection, HTTPS, retention policy, and appropriate privacy notice/consent.

