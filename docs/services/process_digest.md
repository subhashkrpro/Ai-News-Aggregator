# process_digest.py Documentation

## Overview
Processes articles and videos to generate digests using DigestAgent, then stores the results in the database.

## Functions
### process_digests(limit: Optional[int] = None) -> dict
- Fetches articles without digests from the database.
- Uses DigestAgent to generate a summary for each article.
- Stores the digest in the database.
- Returns a summary dict: total, processed, failed.

## Usage Example
```python
from app.services.process_digest import process_digests
result = process_digests()
```

## See Also
- [process_curator.py](process_curator.md)
- [process_email.py](process_email.md)
