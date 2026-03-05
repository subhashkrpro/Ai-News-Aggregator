# repository.py Documentation

## Overview
Implements the Repository class for all database operations, including CRUD for videos, articles, and digests.

## Classes
### Repository
- **__init__(self, session: Optional[Session] = None)**: Initializes with a SQLAlchemy session.
- **create_youtube_video(...)**: Adds a new YouTube video to the database.
- **create_openai_article(...)**: Adds a new OpenAI article.
- **create_anthropic_article(...)**: Adds a new Anthropic article.
- **bulk_create_youtube_videos(videos: List[dict])**: Bulk insert for YouTube videos.
- **bulk_create_openai_articles(articles: List[dict])**: Bulk insert for OpenAI articles.
- **bulk_create_anthropic_articles(articles: List[dict])**: Bulk insert for Anthropic articles.
- **get_anthropic_articles_without_markdown(limit: Optional[int])**: Query for Anthropic articles missing markdown.
- **update_anthropic_article_markdown(guid: str, markdown: str)**: Update markdown for an Anthropic article.
- **get_youtube_videos_without_transcript(limit: Optional[int])**: Query for YouTube videos missing transcript.
- **update_youtube_video_transcript(video_id: str, transcript: str)**: Update transcript for a YouTube video.
- **get_articles_without_digest(limit: Optional[int])**: Query for articles missing a digest.
- **create_digest(...)**: Adds a new digest summary.
- **get_recent_digests(hours: int = 24)**: Query for recent digests.

## Usage Example
```python
from app.database.repository import Repository
repo = Repository()
repo.create_youtube_video(...)
```

## See Also
- [models.py](models.md)
- [connection.py](connection.md)
