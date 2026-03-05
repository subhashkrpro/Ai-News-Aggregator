# digest_agent.py Documentation

## Overview
Implements the DigestAgent class, which summarizes AI news articles, research papers, and videos using an LLM.

## Classes
### DigestAgent
- **__init__(self)**: Initializes the agent with OpenAI API credentials and model.
- **generate_digest(self, title: str, content: str, article_type: str) -> Optional[DigestOutput]**: Uses the LLM to generate a concise title and summary for the given article.

### DigestOutput
- Data model for the digest result (title, summary).

## Constants
- **PROMPT**: Instructions for the LLM to create actionable, informative digests.

## Usage Example
```python
from app.agent.digest_agent import DigestAgent
agent = DigestAgent()
digest = agent.generate_digest(title, content, article_type)
```

## See Also
- [curator_agent.py](../agent/curator_agent.md)
- [email_agent.py](../agent/email_agent.md)
