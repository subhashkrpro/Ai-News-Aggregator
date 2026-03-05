# process_email.py Documentation

## Overview
Generates and sends a daily email digest of ranked AI news articles using CuratorAgent, EmailAgent, and email utilities.

## Functions
### generate_email_digest(hours: int = 24, top_n: int = 10) -> EmailDigestResponse
- Ranks recent digests using CuratorAgent.
- Generates email introduction and digest using EmailAgent.
- Returns an EmailDigestResponse object.

### send_digest_email(hours: int = 24, top_n: int = 10) -> dict
- Generates the email digest and sends it via email.
- Returns a dict with success status, subject, and articles count.

## Usage Example
```python
from app.services.process_email import send_digest_email
result = send_digest_email(hours=24, top_n=10)
```

## See Also
- [email.py](email.md)
- [process_digest.py](process_digest.md)
