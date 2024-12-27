# Journal Application README

## Overview

The **Journal Application** is a RESTful API built using Java, Spring Boot, and MongoDB. It allows users to manage journal entries through standard CRUD operations. The application includes endpoints for creating, reading, updating, and deleting journal entries, with each operation returning appropriate HTTP responses using `ResponseEntity`.

---

## Features

- **Create Journal Entries**: Add new journal entries with a title, content, and timestamp.
- **Retrieve Entries**: Fetch individual or all journal entries.
- **Update Entries**: Modify existing journal entries.
- **Delete Entries**: Remove journal entries permanently.
- **ResponseEntity Integration**: Ensures proper HTTP status codes and response bodies for all operations.

---

## Tech Stack

- **Backend**: Java, Spring Boot
- **Database**: MongoDB
- **Build Tool**: Maven
- **HTTP Responses**: `ResponseEntity` for structured API responses

---

## Prerequisites

- Java Development Kit (JDK 11 or higher)
- MongoDB (Ensure MongoDB is running locally or accessible remotely)
- Maven (for dependency management)

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/journal-application.git
   cd journal-application
   ```

2. Configure MongoDB:
   - Update the `application.properties` file in the `src/main/resources` directory with your MongoDB connection string.

   Example:
   ```properties
   spring.data.mongodb.uri=mongodb://localhost:27017/journalDB
   ```

3. Build and run the application:
   ```bash
   mvn clean install
   mvn spring-boot:run
   ```

4. Access the application at:
   ```
   http://localhost:8080
   ```

---

## API Endpoints

### Base URL: `http://localhost:8080/journal`

| Method   | Endpoint             | Description                              |
|----------|----------------------|------------------------------------------|
| `GET All`    | `/Journal`                  | Retrieve all journal entries.           |
| `GET`    | `/Journal/{id}/{myId}`              | Retrieve a specific journal entry.      |
| `POST`   | `/Journal`                  | Create a new journal entry.             |
| `PUT`    | `/{id}/{myId}`              | Update an existing journal entry.       |
| `DELETE` | `/{id}/{myId}`              | Delete a specific journal entry.        |

---

## Example API Responses

- **GET** `localhost:8080/journal/id/676e855d6a83b91f4dc75294`  
  **Response:**
  ```json
  {
    "id": {
        "timestamp": 1735296349,
        "date": "2024-12-27T10:45:49.000+00:00"
    },
    "title": "Ajay",
    "content": "Frontend developer",
    "date": "2024-12-27T16:15:49.813"
}
  ```

- **POST** `localhost:8080/journal/id/676e855d6a83b91f4dc75294`  
  **Request Body:**
  ```json
  {
    "title": "Ajay",
    "content": "Frontend developer"
  }
  ```
  **Response:**
  ```json
  {
      "id": {
        "timestamp": 1735296349,
        "date": "2024-12-27T10:45:49.000+00:00"
    },
    "title": "Ajay",
    "content": "Frontend developer",
    "date": "2024-12-27T16:15:49.813"
  }
  ```

---

## Contributions

Contributions are welcome! Feel free to submit a pull request or create an issue for any bugs or feature requests.

---

## Contact

For any inquiries or support, reach out to:  
**Developer**: Swarup Kumar Sahoo  
**Email**: [kumarswarup7272@gmail.com]  
**GitHub**: [your-github-profile](https://github.com/swarup-kumar-sahoo)

--- 
