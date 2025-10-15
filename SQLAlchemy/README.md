# SQLAlchemy Package - Connecting to RDBMS Databases

## 🧩 **Part 1 — Foundations of SQLAlchemy**

**Goal:** Understand what SQLAlchemy is and how it works with Python and databases.

1. [**Introduction to SQLAlchemy**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p01.md)

   * What is SQLAlchemy?
   * ORM vs Core
   * Supported databases and installation
   * Architecture overview: Engine, Connection, and Session

2. [**Setting up SQLAlchemy**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p02.md)

   * Installing `SQLAlchemy` and database drivers
   * Creating a database engine (`create_engine()`)
   * Understanding database URLs
   * Basic connection and executing raw SQL

3. [**SQLAlchemy Core Basics**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p03.md)

   * Metadata and Table objects
   * Defining tables with `Table`, `Column`, and `MetaData`
   * Data types (`Integer`, `String`, `DateTime`, etc.)
   * Inserting, selecting, updating, deleting with Core API
   * Using textual SQL (`text()`)

---

## 🧱 **Part 2 — Working with the ORM (Object Relational Mapper)**

**Goal:** Map Python classes to database tables.

4. [**Declarative Base and ORM Mapping**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p04.md)

   * `declarative_base()` and defining models
   * Primary keys and unique constraints
   * Column attributes and relationships
   * Creating tables from ORM models (`Base.metadata.create_all()`)

5. [**CRUD Operations with ORM**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p05.md)

   * Creating a session (`sessionmaker`)
   * Inserting records (`add`, `add_all`, `commit`)
   * Querying (`session.query`, `filter`, `filter_by`)
   * Updating and deleting records

6. [**Relationships Between Tables**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p06.md)

   * One-to-Many, Many-to-One, and Many-to-Many
   * Using `relationship()` and `back_populates`
   * Lazy vs Eager loading
   * Cascades and orphan deletion

7. [**Advanced Querying**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p07.md)

   * Using `select()`, `join()`, and subqueries
   * Aggregations and group by
   * Aliases and labeling
   * Hybrid properties

---

## ⚙️ **Part 3 — Schema, Metadata, and Reflection**

**Goal:** Understand and manipulate the database schema programmatically.

8. [**Metadata Deep Dive**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p08.md)

   * Using `MetaData()` effectively
   * Reflecting existing databases
   * Inspecting tables dynamically (`inspect()`)

9. [**Migrations with Alembic**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p9.md)

   * Introduction to Alembic
   * Creating revision scripts
   * Auto-generating migrations
   * Applying upgrades and downgrades

---

## 🧠 **Part 4 — Best Practices and Advanced Concepts**

**Goal:** Learn how to structure, optimize, and maintain large projects.

10. [**Session Management and Transactions**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p10.md)

    * Transaction scopes
    * Commit and rollback
    * Expiring and refreshing objects
    * Context-managed sessions

11. [**Eager vs Lazy Loading**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p11.md)

    * Performance trade-offs
    * Using `selectinload`, `joinedload`, `subqueryload`

12. [**Events and Hooks**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p12.md)

    * Using `event.listen()`
    * Automating timestamps (created_at, updated_at)
    * Triggers and custom validation

13. [**Optimizations and Performance**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p13.md)

    * Batching and bulk operations
    * Query caching
    * Indexing and constraints
    * Profiling SQL queries

---

## 🧰 **Part 5 — Integration and Real-World Usage**

**Goal:** Use SQLAlchemy effectively in production systems.

14. [**Integration with FastAPI / Flask**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p14.md)

    * Dependency injection with sessions
    * Handling async SQLAlchemy (using `async_engine`)
    * Using Pydantic models with ORM

15. [**Using SQLAlchemy with Databases**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p15.md)

    * SQLite (local testing)
    * PostgreSQL and MySQL configuration
    * Connection pooling

16. [**Testing and CI/CD**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p16.md)

    * Setting up test databases
    * Using fixtures with pytest
    * Mocking sessions and queries

17. [**Packaging and Reusability**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p17.md)

    * Creating a data access layer (DAL)
    * Repository pattern with SQLAlchemy
    * Maintaining models in modular architecture

---

## 🔍 **Part 6 — Hands-On Projects**

**Goal:** Reinforce learning with practical examples.

18. [**Mini Projects**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p18.md)

    * Simple To-Do application
    * Library management system
    * Blog with users and posts

19. [**Advanced Projects**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p19.md)

    * Healthcare patient record system (multi-table ORM)
    * E-commerce order management system
    * FastAPI + SQLAlchemy + Alembic full-stack app

20. [**Deployment**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/SQLAlchemy/p20.md)

    * Using Docker with PostgreSQL and SQLAlchemy
    * Running migrations automatically on startup
    * Managing environment variables securely

---

