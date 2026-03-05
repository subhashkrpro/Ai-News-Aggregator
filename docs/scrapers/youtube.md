# youtube.py Documentation

## Overview
Implements the YouTubeScraper class to fetch YouTube videos and transcripts from specified channels using RSS feeds and the YouTube Transcript API.

## Classes
### YouTubeScraper
- **__init__(self)**: Initializes with optional proxy configuration for transcript API.
- **get_latest_videos(self, channel_id: str, hours: int = 24) -> list[ChannelVideo]**: Fetches videos published within the last `hours` from a channel.
- **get_transcript(self, video_id: str) -> Optional[Transcript]**: Fetches transcript for a given video ID.
- **scrape_channel(self, channel_id: str, hours: int = 150) -> list[ChannelVideo]**: Fetches videos and their transcripts for a channel.

### ChannelVideo
- Data model for a YouTube video (title, url, video_id, published_at, description, transcript).

### Transcript
- Data model for a video transcript (text).

## Usage Example
```python
from app.scrapers.youtube import YouTubeScraper
scraper = YouTubeScraper()
videos = scraper.get_latest_videos(channel_id, hours=24)
transcript = scraper.get_transcript(video_id)
```

## See Also
- [anthropic.py](anthropic.md)
- [openai.py](openai.md)
