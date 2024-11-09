
# Task Manager API

This is a RESTful API for managing tasks in a task management application. The API is built with Spring Boot and includes endpoints for creating, retrieving, updating, and deleting tasks. Additionally, the application has JWT-based authentication for securing API requests.

## Features

- **Task Management**: Create, view, update, and delete tasks.
- **JWT Authentication**: Secures endpoints, requiring valid tokens for access.
- **RESTful API**: Exposes well-structured endpoints.

## Technologies Used

- Java
- Spring Boot
- Spring Security
- JPA (Java Persistence API)
- JWT (JSON Web Token)
- MySQL (or other supported databases)

## Getting Started

### Prerequisites

- Java 11 or higher
- Maven or Gradle
- MySQL Database (or configure another database in `application.properties`)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/task-manager.git
   ```

2. Navigate into the project directory:

   ```bash
   cd task-manager
   ```

3. Update the `application.properties` file with your database credentials.

4. Build the project:

   ```bash
   mvn clean install
   ```

5. Run the application:

   ```bash
   mvn spring-boot:run
   ```

### API Endpoints

| Method | Endpoint       | Description                |
| ------ | -------------- | -------------------------- |
| POST   | `/api/tasks`   | Create a new task          |
| GET    | `/api/tasks`   | Get all tasks              |
| GET    | `/api/tasks/{id}` | Get task by ID           |
| PUT    | `/api/tasks/{id}` | Update task by ID       |
| DELETE | `/api/tasks/{id}` | Delete task by ID       |

### JWT Authentication

1. Upon login, the server returns a JWT token.
2. Include this token in the `Authorization` header with the prefix "Bearer" to access protected routes.

### Example

- **Create Task**:
  ```bash
  curl -X POST http://localhost:8080/api/tasks -H "Authorization: Bearer <JWT_TOKEN>" -d '{"name":"Task 1","description":"Sample Task","status":"TO_DO"}' -H "Content-Type: application/json"
  ```

## License

This project is licensed under the MIT License - see the LICENSE file for details.
