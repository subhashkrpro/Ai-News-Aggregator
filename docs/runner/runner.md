# runner.py Documentation

## Overview
Runs all scrapers for YouTube, OpenAI, and Anthropic, and stores results in the database.

## Functions
### run_scrapers(hours: int = 24) -> dict
- Scrapes YouTube videos, OpenAI articles, and Anthropic articles for the last `hours`.
- Stores results in the database using Repository.
- Returns a dict with lists of scraped items for each source.

## Usage Example
```python
from app.runner import run_scrapers
results = run_scrapers(hours=24)
```

## See Also
- [config.py](config.md)
- [daily_runner.py](daily_runner.md)
