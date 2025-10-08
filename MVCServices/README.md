# **MVC (Model-View-Controller) with Dash & Streamlit**

# Part 1 — Core Foundations (applies to both Dash & Streamlit)

1. [**Project Structure & Layering**](#)

* Goal: Keep UI, controller, and model cleanly separated.
* Learn: folder layout; import boundaries; avoiding cycles.
* Lab: Take a single-file toy app and split into `views/`, `controllers/`, `models/`.

2. [**DTOs with Pydantic**](#)

* Goal: Stable request/response shapes between layers.
* Learn: `BaseModel`, `Field()`, validators, `model_dump()`.
* Lab: Define `CustomerCreate`, `CustomerRead`, `OrderCreate`; convert a pandas row → DTO.

3. [**Repositories (I/O only)**](#)

* Goal: All DB/API/file access in one place.
* Learn: SQLAlchemy engine/session factory; CRUD patterns; query functions that return rows/DTOs.
* Lab: Build `repositories.py` with `list_customers()`, `create_order()`.

4. [**Services (business rules)**](#)

* Goal: Keep logic pure & testable; no UI imports.
* Learn: input validation, orchestration across repositories, returned DTOs/dataframes.
* Lab: `calculate_invoice_totals(lines, tax_rate)` (pure function) + unit tests.

5. [**Dependency Injection & Testing**](#)

* Goal: Test services without a real DB.
* Learn: pass repository interfaces; fakes/mocks; pytest fixtures.
* Lab: Test `get_sales_summary(year)` using a fake repo.

6. [**Config & Environments**](#)

* Goal: Reproducible setups for dev/test/prod.
* Learn: `.env`, `pydantic-settings`, config objects.
* Lab: Build `config/settings.py` with DB URL, feature flags.

7. [**Error Handling & Logging**](#)

* Goal: Predictable failures + useful logs.
* Learn: custom exceptions (e.g., `DomainError`), structured logs, error boundaries.
* Lab: Make services raise `ValidationError`; log in controllers.

---

# Part 2 — Dash Track (controller = callbacks)

8. [**View Layer in Dash**](#)

* Learn: compose `html.*`, `dcc.*`, reusable layout functions.
* Lab: `views/dashboard.py` returning a card grid + table builder.

9. [**Controller Layer: Callbacks**](#)

* Learn: `@callback(Input, Output, State)`, PreventUpdate, pattern-matching IDs.
* Lab: Button → service call → update DataTable.

10. [**Multipage Apps**](#)

* Learn: page registry, per-page layouts, page-scoped callbacks.
* Lab: Add `/inventory` page + dedicated callbacks file.

11. [**State & Performance**](#)

* Learn: clientside callbacks, memoization, long callbacks/spinners.
* Lab: Cache service function; show spinner while loading.

---

# Part 3 — Streamlit Track (controller = actions + session_state)

12. [**View Layer in Streamlit**](#)

* Learn: `st.columns`, `st.dataframe`, modular section functions.
* Lab: `views/sections.py` with `render_filters()`, `render_table(df)`.

13. [**Controller Layer: Actions + Session State**](#)

* Learn: event handlers, `st.session_state` lifecycle, rerun flow.
* Lab: `controllers/actions.py` that sets `session_state["data"]` after calling a service.

14. [**Multipage Apps**](#)

* Learn: pages folder, cross-page state, query params.
* Lab: `1_Dashboard.py`, `2_Patients.py` using shared controllers/views.

15. [**Caching & Performance**](#)

* Learn: `@st.cache_data`, `@st.cache_resource`, invalidation keys.
* Lab: Cache `services.list_patients()`; clear when write happens.

---

# Part 4 — Cross-Cutting Enhancements

16. [**Async Services (optional)**](#)

* Learn: `async` repositories with HTTP APIs or async DB drivers; threading vs asyncio.
* Lab: Fetch two APIs concurrently; merge results in a service.

17. [**Auth & Permissions (lightweight)**](#)

* Dash: protect routes or components based on a user role.
* Streamlit: simple login gate + role in session_state.
* Lab: Hide admin sections unless role == "admin".

18. [**Validation & Security**](#)

* Learn: defensive checks in services; sanitize inputs; limit query sizes.
* Lab: Reject orders with negative quantities; clamp pagination.

19. [**Packaging & Reuse**

* Learn: turn `models/` into an installable package for multiple apps.
* Lab: Create `pyproject.toml`; import services from another app.

20. **CI/CD & Quality Gates**](#)

* Learn: pytest, coverage, ruff/flake8, mypy, pre-commit.
* Lab: Add GitHub Actions workflow to run tests + lint + type-check.

21. [**Docs & Onboarding**](#)

* Learn: README patterns, architecture diagram, ADRs (decision records).
* Lab: Add a “How to add a new page/service” guide to README.

---

## Reading & Editing Generated Code — Checklist

* **Views**: only UI code? no DB/API calls? small pure functions that accept data?
* **Controllers**: orchestrate only? import `services` (not `repositories`)? handle errors & set state?
* **Services**: pure, typed; raise domain errors; return DTOs/dataframes; unit tests exist?
* **Repositories**: I/O only; no business logic; test with a temp SQLite file or fakes.
* **Schemas**: consistent DTOs; default values & validators defined?
* **Config**: no secrets hard-coded; `.env` used; sensible defaults.
* **Imports**: no cycles; views → controllers? (should be opposite: pages import both; controllers do not import views unless passing data to view helpers)

---

## Mini Capstones (pick one)

* **SalesSuite (Dash)**: dashboard, customers, orders, inventory; add **“export CSV”** service + callback; test services.
* **ClinicBoard (Streamlit)**: dashboard, appointments, patients; add **“bulk upload patients”** (CSV → DTO → service → repo) with cache invalidation.

---

## Practice Prompts (drop-in)

* *“Generate a Streamlit multipage app in MVC + service-controller style with pages X,Y,Z. Use SQLAlchemy+SQLite. Include repositories, services, schemas, controllers(actions), views(sections). Provide unit tests for services and a README.”*

* *“Add a new page ‘inventory’ using the same structure. Views define filters & table; controller reads inputs and calls `services.get_inventory_summary` (no business logic in controller). Update routes/pages and seed sample data.”*

* *“Refactor this single-file app to MVC. Extract repositories, services, DTOs; keep UI unchanged; add tests for services.”* (paste code)

---

## Suggested Study Order (quick)

1. DTOs + Repositories → Services → Unit Tests
2. Views → Controllers (Dash callbacks / Streamlit actions)
3. Multipage → Caching/Performance → Auth → CI/CD

---

If you tell me which track you want to start with (**Dash or Streamlit**) and your first 2–3 pages/entities, I’ll spin up a **starter repo** (files + tests + README) following this curriculum so you can learn by editing real code.
