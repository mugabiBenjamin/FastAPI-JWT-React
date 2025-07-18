# backend/README.md

## Installation

```bash
uv sync
```

## Usage

```bash
source .venv/bin/activate

uv run uvicorn main:app --reload

# OR traditional
uvicorn main:app --reload
```

## Project Structure

```plaintext
.
├── app                             # Main application package
│   ├── api                         # API routing and endpoints
│   │   └── v1                      # Version 1 of the API
│   │       └── endpoints           # API endpoint implementations
│   ├── core                        # Core settings, config, and utilities
│   ├── models                      # Database models
│   ├── schemas                     # Pydantic schemas for data validation
│   └── services                    # Business logic and service layer
├── attendance.db                   # SQLite database file
├── main.py                         # Application entry point
├── pyproject.toml                  # Project dependencies and metadata
├── README.md                       # Project documentation
└── uv.lock                         # Dependency lock file for uv
```

## Environment Variables

Create a `.env` file and add the following environment variables:

```env
SECRET_KEY=your_key_here
DATABASE_URL=sqlite:///./dbname.db
FRONTEND_URL=http://localhost:3000
ENVIRONMENT=development
ACCESS_TOKEN_EXPIRE_MINUTES=30

# For PostgreSQL: postgresql://username:password@localhost/dbname
# For MySQL: mysql://username:password@localhost/dbname
```

## Generate a Secret Key

```bash
python -c "import secrets; print(secrets.token_hex(32))"

# Or use the OpenSSL command:
openssl rand -hex 32

# Both generate a 32-byte hex string. Copy the output and use it as your SECRET_KEY in the auth file.
```

## Note -> `bcrypt 4.3.0+` has breaking changes with passlib
