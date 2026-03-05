# process_anthropic.py Documentation

## Overview
Processes Anthropic articles by converting their URLs to markdown and updating the database.

## Functions
### process_anthropic_markdown(limit: Optional[int] = None) -> dict
- Fetches Anthropic articles missing markdown from the database.
- Converts each article's URL to markdown.
- Updates the database with the markdown content.
- Returns a summary dict: total, processed, failed.

## Usage Example
```python
from app.services.process_anthropic import process_anthropic_markdown
result = process_anthropic_markdown()
```

## See Also
- [email.py](email.md)
- [process_youtube.py](process_youtube.md)
