# 📘 FastAPI Development – Beginner to Advanced

## 1. [**Introduction & Fundamentals**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p01.md)

* What is FastAPI?
* Advantages over Flask/Django (speed, async, type hints).
* Installing FastAPI and Uvicorn.
* First "Hello World" example.
* FastAPI project folder structure.

---

## 2. [**Core Building Blocks**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p02.md)

* Path parameters (e.g., `/items/{id}`).
* Query parameters (e.g., `/items?name=apple&price=10`).
* Request body with **Pydantic models**.
* Handling multiple request bodies.
* Response models and data validation.
* Example: Simple CRUD for `Book` API.

---

## 3. [**Data Validation & Serialization**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p03.md)

* Field validation with **Pydantic** (`min_length`, `regex`, `ge`, `le`).
* Nested models.
* Default values & optional fields.
* Custom validators with `@validator`.
* Example: Validating user registration request (email, password rules).

---

## 4. [**Dependency Injection**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p04.md)

* `Depends()` function for reusable logic.
* Using dependencies for authentication.
* Parameterized dependencies.
* Example: Injecting database session into routes.

---

## 5. [**Request Handling**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p05.md)

* Form data submission (`Form`).
* File uploads (`File`, `UploadFile`).
* Handling JSON, text, and binary requests.
* Example: Profile upload API with image + form fields.

---

## 6. [**Response Handling**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p06.md)

* Custom response types (`JSONResponse`, `HTMLResponse`, `PlainTextResponse`).
* Streaming responses.
* Returning files (CSV, PDF, images).
* Example: Export data to CSV endpoint.

---

## 7. [**Authentication & Authorization**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p07.md)

* Basic authentication.
* OAuth2 with password flow.
* JWT (JSON Web Tokens) authentication.
* Role-based access control (RBAC).
* Example: Login + Protected routes with JWT tokens.

---

## 8. [**Database Integration**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p08.md)

* SQL Databases (SQLite, PostgreSQL, MySQL) with **SQLAlchemy**.
* ORM with **SQLModel** (FastAPI-native ORM).
* Async databases (`Databases` package, Tortoise ORM).
* Example: Full CRUD with SQLAlchemy and Pydantic schemas.

---

## 9. [**Background Tasks & Scheduling**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p09.md)

* Using `BackgroundTasks` for sending emails, logs.
* Async tasks with Celery & Redis.
* Scheduled jobs with APScheduler.
* Example: User registration triggers welcome email in background.

---

## 10. [**Middleware**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p10.md)

* Custom middleware.
* CORS setup.
* Logging middleware.
* Example: Logging request execution time.

---

## 11. [**Error Handling**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p11.md)

* Raising `HTTPException`.
* Custom exception handlers.
* Global error handling middleware.
* Example: Custom JSON response for 404 errors.

---

## 12. [**Testing**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p12.md)

* Testing with **pytest**.
* Using `TestClient` from FastAPI.
* Mocking database & dependencies.
* Example: Unit tests for CRUD routes.

---

## 13. [**Asynchronous Programming**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p13.md)

* `async` vs `sync` routes.
* Async database queries.
* Running blocking tasks in threads.
* Example: Fetching data from external API asynchronously.

---

## 14. [**WebSockets & Real-Time Apps**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p14.md)

* WebSocket routes in FastAPI.
* Building a chat app with WebSockets.
* Example: Real-time notification system.

---

## 15. [**Event Handling**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p15.md)

* Startup & shutdown events.
* Database connection pooling.
* Example: Initialize DB on startup, close session on shutdown.

---

## 16. [**FastAPI with Frontend**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p16.md)

* Returning HTML templates with Jinja2.
* Serving static files.
* Example: Simple blog app with HTML templates.

---

## 17. [**Security Features**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p17.md)

* Password hashing with **bcrypt**.
* CSRF protection.
* OAuth2 scopes.
* Example: Secure API with JWT + role-based permissions.

---

## 18. [**Documentation & Schema**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p18.md)

* OpenAPI & Swagger UI.
* API docs with Redoc.
* Customizing docs & metadata.
* Example: Adding API description and tags for endpoints.

---

## 19. [**Microservices & Scaling**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p19.md)

* FastAPI in Docker.
* API Gateway design with FastAPI.
* Service-to-service communication (REST & gRPC).
* Example: Microservice for payments with FastAPI.

---

## 20. [**Performance & Optimization**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p20.md)

* Using async properly.
* Connection pooling for DB.
* Caching with Redis.
* Gunicorn + Uvicorn workers.
* Example: Caching frequently requested data.

---

## 21. [**Advanced Features**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p21.md)

* Custom decorators.
* Event-driven design with Kafka/RabbitMQ.
* GraphQL with FastAPI.
* Example: GraphQL API with Strawberry + FastAPI.

---

## 22. [**Deployment**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p22.md)

* Deploying with Docker & Docker Compose.
* Deploying on AWS/GCP/Azure.
* CI/CD with GitHub Actions.
* Example: FastAPI + PostgreSQL + Nginx deployment.

---

## 23. [**Case Studies & Projects**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/FastAPI/p23.md)

* RESTful Todo API.
* Authentication System with JWT.
* E-commerce backend (users, products, orders).
* Healthcare API (patients, appointments, prescriptions).
* Real-time chat app with WebSockets.

---

👉 This progression ensures you **start from basics and gradually reach enterprise-level FastAPI applications** with real-world examples.



