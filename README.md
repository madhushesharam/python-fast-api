
## Project Name: FastAPI User Management System

## Overview

This project implements a user management system using FastAPI and SQLAlchemy.

Perform CRUD operations (Create, Read, Update, Delete) on user records stored in a database.


### Architecture Diagram Workflow

```plaintext
+--------+         +----------------+        +------------+         +----------+
| Client | <-----> |   FastAPI      |        | SQLAlchemy | <-----> | Database |
|        |         | - Endpoints    |        | - Models   |         | - Tables |
|        |         | - Request      |        | - Sessions |         | - Records|
|        |         |   Handling     |        | - Queries  |         |          |
+--------+         +----------------+        +------------+         +----------+
```



### Features

- **API Endpoints**:
  - `/users/`: Get all users (with pagination)
  - `/users/{user_id}`: Get user by ID
  - `/users/email/{user_email}`: Get user by email
  - `/users/`: Create a new user
  - `/users/`: Update an existing user
  - `/users/{user_id}`: Delete a user

- **Database Management**:
  - Uses SQLite for local development (`sql_app.db`)
  - SQLAlchemy ORM manages database interactions, including schema creation, querying, and transactions.

- **Error Handling**:
  - Proper HTTP status codes and error messages for invalid requests or non-existent resources.

- **Testing**:
  - Includes unit tests to validate API endpoints and database operations.
  - Uses `pytest` framework for testing.

### Installation

1. **Clone the repository:**

   ```bash
   git clone <repository-url>
   cd fastapi-user-management
   ```

2. **Install dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the application:**

   ```bash
   docker build -t fastapi-user-management .
   docker run -d -p 8000:8000 fastapi-user-management
   ```

   Access the API at `http://localhost:8000`.


4. Package and distribute 
    docker build -t fastapi-app -f Containerfile
    docker run -d -p 8000:8000 fastapi-app # local test 



### Usage

- Use an API client (e.g., `curl`, Postman) to interact with the endpoints.
- Detailed API documentation is available at `http://localhost:8000/docs`.



### Credits

- FastAPI: [https://fastapi.tiangolo.com/](https://fastapi.tiangolo.com/)
- SQLAlchemy: [https://www.sqlalchemy.org/](https://www.sqlalchemy.org/)



## TODO : Add Unit tests, JWT Auth, SCA, Scans , pipeline etc.