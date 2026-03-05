# AI News Aggregator

## Overview

AI News Aggregator is a Python application that automatically collects, summarizes, ranks, and delivers daily digests of AI news, research, and videos. It gathers content from YouTube, OpenAI, and Anthropic, processes and ranks articles using AI agents, and sends a personalized email digest to the user.

## Features

- Scrapes the latest AI news from YouTube, OpenAI, and Anthropic
- Extracts YouTube video transcripts
- Summarizes articles and videos using LLM-powered agents
- Ranks content based on your profile and interests
- Generates and sends daily email digests
- Stores all data in a PostgreSQL database

## Project Structure

- `main.py`: Entry point for running the daily pipeline
- `app/`
  - `daily_runner.py`: Orchestrates the daily pipeline
  - `runner.py`: Runs all scrapers and stores results
  - `config.py`: Configuration (e.g., YouTube channels)
  - `agent/`: AI agents for curation, digest, and email generation
  - `database/`: SQLAlchemy models, connection, and repository
  - `profiles/`: User profile for personalized ranking
  - `scrapers/`: Scrapers for YouTube, OpenAI, Anthropic
  - `services/`: Processing modules for each source and email
- `docker/docker-compose.yml`: PostgreSQL service for development

## Installation

1. **Clone the repository**
2. **Install Python 3.13+**
3. **Install dependencies with [uv](https://github.com/astral-sh/uv):**
	```sh
	uv sync
	```
4. **Set up environment variables:**
	- Copy `.env.example` to `.env` and fill in your API keys, email, and database credentials.
5. **Start PostgreSQL (optional, for local development):**
	```sh
	docker compose -f docker/docker-compose.yml up -d
	```
6. **Create database tables:**
	```sh
	uv run python app/database/create_tables.py
	```

## Usage

Run the daily pipeline (default: last 24 hours, top 10 articles):

```sh
uv run python main.py [hours] [top_n]
```

Example:
```sh
uv run python main.py 24 10
```

## Configuration

- **User Profile:** Edit `app/profiles/user_profile.py` to customize interests and preferences.
- **YouTube Channels:** Add channel IDs in `app/config.py`.
- **Environment Variables:** See `.env.example` for required keys.

## Agents

- **Curator Agent:** Ranks digests based on your profile.
- **Digest Agent:** Summarizes articles and videos.
- **Email Agent:** Generates personalized email introductions and digests.

## Database

- Uses PostgreSQL (see `docker/docker-compose.yml`)
- Models defined in `app/database/models.py`

## Dependencies

- See `pyproject.toml` for all required packages
- Uses [uv](https://github.com/astral-sh/uv) for fast dependency management
