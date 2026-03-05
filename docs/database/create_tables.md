# create_tables.py Documentation

## Overview
Script to create all database tables using SQLAlchemy models and engine.

## Usage
Run this script to initialize the database tables:
```sh
python app/database/create_tables.py
```

## Main Logic
- Imports SQLAlchemy Base and engine
- Calls `Base.metadata.create_all(engine)` to create tables

## See Also
- [models.py](models.md)
- [connection.py](connection.md)
