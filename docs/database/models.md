# models.py Documentation

## Overview
Defines SQLAlchemy ORM models for all database tables used in the AI News Aggregator.

## Classes
### YouTubeVideo
Represents a YouTube video and its metadata.
- Fields: video_id, title, url, channel_id, published_at, description, transcript, created_at

### OpenAIArticle
Represents an OpenAI news article.
- Fields: guid, title, url, description, published_at, category, created_at

### AnthropicArticle
Represents an Anthropic news article.
- Fields: guid, title, url, description, published_at, category, markdown, created_at

### Digest
Represents a digest summary for an article or video.
- Fields: id, article_type, article_id, url, title, summary, created_at

## Usage Example
```python
from app.database.models import YouTubeVideo, OpenAIArticle, AnthropicArticle, Digest
```

## See Also
- [connection.py](connection.md)
- [repository.py](repository.md)
