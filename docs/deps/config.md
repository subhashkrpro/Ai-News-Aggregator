# config.py Documentation

## Overview
Defines configuration constants for the AI News Aggregator.

## Variables
### YOUTUBE_CHANNELS
- List of YouTube channel IDs to scrape for AI news videos.

## Usage Example
```python
from app.config import YOUTUBE_CHANNELS
for channel_id in YOUTUBE_CHANNELS:
    print(channel_id)
```

## See Also
- [runner.py](runner.md)
- [daily_runner.py](daily_runner.md)
