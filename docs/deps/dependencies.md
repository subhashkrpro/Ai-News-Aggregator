# Dependencies Documentation

## Overview
This project uses modern Python libraries for web scraping, data processing, database management, and AI integration. Dependencies are managed with [uv](https://github.com/astral-sh/uv) for fast, reliable installs.

## How to Install
Install all dependencies with:
```sh
uv sync
```

## Main Dependencies
- **beautifulsoup4**: HTML/XML parsing
- **docling**: Document conversion and markdown export
- **feedparser**: RSS feed parsing
- **markdown, markdownify**: Markdown processing and conversion
- **openai**: OpenAI API client for LLM agents
- **psycopg2-binary**: PostgreSQL database driver
- **pydantic**: Data validation and modeling
- **python-dotenv**: Environment variable management
- **requests**: HTTP requests
- **sqlalchemy**: ORM for database models and queries
- **youtube-transcript-api**: Fetch YouTube video transcripts

## Development Dependencies
- **ipykernel**: Jupyter kernel for development and notebooks

## Where to Find
All dependencies are listed in `pyproject.toml` under `[project]` and `[dependencies-groups]`.

## Example
```toml
[project]
dependencies = [
    "beautifulsoup4>=4.14.2",
    ...
]

[dependencies-groups]
dev = [
    "ipykernel>=7.1.0",
]
```

## See Also
- [pyproject.toml](../pyproject.toml)
- [README.md](../README.md)
