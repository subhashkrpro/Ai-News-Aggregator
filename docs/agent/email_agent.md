# email_agent.py Documentation

## Overview
Implements the EmailAgent class, which generates personalized email digests and introductions for AI news using an LLM.

## Classes
### EmailAgent
- **__init__(self, user_profile: dict)**: Initializes the agent with OpenAI API credentials, model, and user profile.
- **generate_introduction(self, ranked_articles: List) -> EmailIntroduction**: Generates a greeting and introduction for the email digest.
- **create_email_digest(self, ranked_articles: List[dict], limit: int = 10) -> EmailDigest**: Creates an email digest with introduction and ranked articles.
- **create_email_digest_response(self, ranked_articles: List[RankedArticleDetail], total_ranked: int, limit: int = 10) -> EmailDigestResponse**: Returns a detailed email digest response.

### EmailIntroduction
- Data model for the email greeting and introduction.

### RankedArticleDetail
- Data model for details of a ranked article in the email digest.

### EmailDigestResponse
- Data model for the full email digest response.

### EmailDigest
- Data model for the email digest with introduction and ranked articles.

## Constants
- **EMAIL_PROMPT**: Instructions for the LLM to generate professional, engaging email introductions.

## Usage Example
```python
from app.agent.email_agent import EmailAgent
agent = EmailAgent(user_profile)
intro = agent.generate_introduction(ranked_articles)
digest = agent.create_email_digest_response(ranked_articles, total_ranked, limit=10)
```

## See Also
- [curator_agent.py](../agent/curator_agent.md)
- [digest_agent.py](../agent/digest_agent.md)
