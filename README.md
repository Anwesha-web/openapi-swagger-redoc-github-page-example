# End-to-End API Documentation Workflow

This project demonstrates a **complete API documentation workflow** using modern OpenAPI tooling.

It shows how to write, validate, test, and publish API documentation using industry-standard tools.

## Tools Used

• OpenAPI 3
• Swagger Editor
• Swagger UI
• Redoc
• Redocly CLI
• Postman
• GitHub Pages

These tools are widely used by companies such as **Stripe, PayPal, Microsoft, and Google** to build developer-friendly API documentation.

---

# Project Structure

```
api-docs-project
│
├── openapi
│   └── openapi.yaml
│
├── docs
│   ├── swagger-ui.html
│   └── redoc.html
│
├── examples
│   └── user-request.json
│
└── README.md
```

### Folder Explanation

| Folder    | Purpose                            |
| --------- | ---------------------------------- |
| openapi   | Contains the OpenAPI specification |
| docs      | Documentation UI files             |
| examples  | Example API requests               |
| README.md | Project documentation              |

---

# OpenAPI Specification

The API specification is written using **OpenAPI 3.0**.

Location:

```
openapi/openapi.yaml
```

The specification defines:

• API endpoints
• request parameters
• request body schemas
• response models
• authentication
• error responses

---

# API Endpoints

| Method | Endpoint    | Description            |
| ------ | ----------- | ---------------------- |
| GET    | /users      | Retrieve list of users |
| POST   | /users      | Create a new user      |
| GET    | /users/{id} | Retrieve a user by ID  |
| DELETE | /users/{id} | Delete a user          |

---

# Example Request

```
POST /users
```

Request body:

```json
{
  "name": "John Doe",
  "email": "john@example.com"
}
```

---

# Example Response

```
201 Created
```

```json
{
  "id": 1,
  "name": "John Doe",
  "email": "john@example.com"
}
```

---

# Run Documentation Locally

Start a local server:

```
python -m http.server 8000
```

Open documentation:

Swagger UI

```
http://localhost:8000/docs/swagger-ui.html
```

Redoc

```
http://localhost:8000/docs/redoc.html
```

---

# Validate OpenAPI Specification

This project uses **Redocly CLI** to validate the OpenAPI file.

Run:

```
redocly lint openapi/openapi.yaml
```

Example output:

```
openapi.yaml: validated successfully
```

---

# API Testing

API endpoints can be tested using **Postman**.

Example request:

```
GET https://api.example.com/v1/users
```

Postman allows you to inspect:

• response body
• status codes
• headers

---

# Publish Documentation

Documentation can be hosted using **GitHub Pages**.

Example URLs:

Swagger UI

```
https://username.github.io/api-docs-project/docs/swagger-ui.html
```

Redoc

```
https://username.github.io/api-docs-project/docs/redoc.html
```

---

# Documentation Workflow

The documentation workflow used in this project:

```
OpenAPI Specification
        │
        ▼
Swagger Editor
        │
        ▼
Redocly CLI Validation
        │
        ▼
Swagger UI + Redoc
        │
        ▼
Postman API Testing
        │
        ▼
GitHub Pages Deployment
```

---

# Why This Project Matters

Good API documentation improves:

• developer experience
• integration speed
• API adoption
• maintainability

Modern teams treat documentation as **code** using a **Docs-as-Code workflow**.

---

# Author

API Documentation Example Project

