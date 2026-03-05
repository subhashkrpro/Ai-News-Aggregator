# anthropic.py Documentation

## Overview
Implements the AnthropicScraper class to fetch and process Anthropic news articles from multiple RSS feeds.

## Classes
### AnthropicScraper
- **__init__(self)**: Initializes with RSS feed URLs and a document converter.
- **get_articles(self, hours: int = 24) -> List[AnthropicArticle]**: Fetches articles published within the last `hours` from all feeds.
- **url_to_markdown(self, url: str) -> Optional[str]**: Converts an article URL to markdown using the document converter.

### AnthropicArticle
- Data model for an Anthropic news article (title, description, url, guid, published_at, category).

## Usage Example
```python
from app.scrapers.anthropic import AnthropicScraper
scraper = AnthropicScraper()
articles = scraper.get_articles(hours=24)
markdown = scraper.url_to_markdown(articles[0].url)
```

## See Also
- [openai.py](openai.md)
- [youtube.py](youtube.md)
