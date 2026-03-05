# process_youtube.py Documentation

## Overview
Processes YouTube videos by fetching transcripts and updating the database.

## Functions
### process_youtube_transcripts(limit: Optional[int] = None) -> dict
- Fetches YouTube videos missing transcripts from the database.
- Uses YouTubeScraper to fetch transcripts.
- Updates the database with transcript or marks as unavailable.
- Returns a summary dict: total, processed, unavailable, failed.

## Usage Example
```python
from app.services.process_youtube import process_youtube_transcripts
result = process_youtube_transcripts()
```

## See Also
- [process_anthropic.py](process_anthropic.md)
- [process_digest.py](process_digest.md)
