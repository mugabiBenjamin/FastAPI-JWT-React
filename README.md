# FastAPI JWT React App

## Project Structure

```plaintext
└── fastapi-jwt-react/
    ├── README.md                       # Project overview and instructions
    └── backend/
        ├── README.md                   # Backend-specific documentation
        ├── main.py                     # FastAPI application entry point
        ├── pyproject.toml              # Project metadata and dependencies
        ├── uv.lock                     # Locked dependency versions (for uv)
        ├── .python-version             # Python version specification
        └── app/
            ├── api/                    # API routing and endpoint definitions
            │   └── v1/                 # Version 1 of the API
            │       └── endpoints/      # Individual API endpoint modules
            ├── core/                   # Core app configuration and utilities
            ├── models/                 # Database models and ORM classes
            ├── schemas/                # Pydantic schemas for data validation
            └── services/               # Business logic and service layer
```
