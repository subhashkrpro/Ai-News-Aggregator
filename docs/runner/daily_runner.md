# daily_runner.py Documentation

## Overview
Orchestrates the full daily pipeline for scraping, processing, digest creation, and email delivery.

## Functions
### run_daily_pipeline(hours: int = 24, top_n: int = 10) -> dict
- Runs all steps: scraping, processing, digest creation, and email sending.
- Logs progress and results.
- Returns a summary dict with results for each step.

## Usage Example
```python
from app.daily_runner import run_daily_pipeline
result = run_daily_pipeline(hours=24, top_n=10)
```

## See Also
- [runner.py](runner.md)
- [process_email.py](services/process_email.md)
