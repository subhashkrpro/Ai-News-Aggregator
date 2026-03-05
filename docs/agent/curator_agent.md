# curator_agent.py Documentation

## Overview
Implements the CuratorAgent class, which ranks AI news digests based on a user's profile, interests, and preferences using an LLM.

## Classes
### CuratorAgent
- **__init__(self, user_profile: dict)**: Initializes the agent with OpenAI API credentials, model, and user profile.
- **_build_system_prompt(self) -> str**: Builds a system prompt for the LLM using the user's interests and preferences.
- **rank_digests(self, digests: List[dict]) -> List[RankedArticle]**: Ranks a list of digests by relevance using the LLM.

### RankedArticle
- Data model for a ranked digest article (id, relevance_score, rank, reasoning).

### RankedDigestList
- Data model for a list of ranked articles.

## Constants
- **CURATOR_PROMPT**: Instructions for the LLM to rank articles based on user profile and criteria.

## Usage Example
```python
from app.agent.curator_agent import CuratorAgent
agent = CuratorAgent(user_profile)
ranked = agent.rank_digests(digests)
```

## See Also
- [digest_agent.py](../agent/digest_agent.md)
- [email_agent.py](../agent/email_agent.md)
