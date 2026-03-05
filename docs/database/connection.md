# connection.py Documentation

## Overview
Handles database connection setup for the AI News Aggregator using SQLAlchemy and environment variables.

## Functions
### get_database_url() -> str
Builds the PostgreSQL database URL from environment variables.

### get_session()
Returns a new SQLAlchemy session for database operations.

## Variables
- **engine**: SQLAlchemy engine instance.
- **SessionLocal**: SQLAlchemy session factory.

## Usage Example
```python
from app.database.connection import get_session
session = get_session()
```

## See Also
- [models.py](models.md)
- [repository.py](repository.md)
