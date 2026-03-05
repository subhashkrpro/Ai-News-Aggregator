# openai.py Documentation

## Overview
Implements the OpenAIScraper class to fetch and process OpenAI news articles from the OpenAI RSS feed.

## Classes
### OpenAIScraper
- **__init__(self)**: Initializes with the OpenAI RSS feed URL and a document converter.
- **get_articles(self, hours: int = 24) -> List[OpenAIArticle]**: Fetches articles published within the last `hours`.

### OpenAIArticle
- Data model for an OpenAI news article (title, description, url, guid, published_at, category).

## Usage Example
```python
from app.scrapers.openai import OpenAIScraper
scraper = OpenAIScraper()
articles = scraper.get_articles(hours=24)
```

## See Also
- [anthropic.py](anthropic.md)
- [youtube.py](youtube.md)
