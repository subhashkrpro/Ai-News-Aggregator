# process_curator.py Documentation

## Overview
Curates and ranks AI news digests using the CuratorAgent and user profile, then logs and returns the results.

## Functions
### curate_digests(hours: int = 24) -> dict
- Fetches recent digests from the database.
- Ranks digests using CuratorAgent and user profile.
- Logs top ranked articles and reasoning.
- Returns a summary dict: total, ranked, articles.

## Usage Example
```python
from app.services.process_curator import curate_digests
result = curate_digests(hours=24)
```

## See Also
- [process_digest.py](process_digest.md)
- [process_email.py](process_email.md)
