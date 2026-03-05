# user_profile.py Documentation

## Overview
Defines the USER_PROFILE dictionary for personalized content ranking and email generation.

## USER_PROFILE Fields
- **name**: User's name
- **title**: Professional title
- **background**: Brief background description
- **interests**: List of AI topics and interests
- **preferences**: Dict of user preferences (e.g., prefer_practical, prefer_technical_depth)
- **expertise_level**: User's expertise level (e.g., Advanced)

## Usage Example
```python
from app.profiles.user_profile import USER_PROFILE
print(USER_PROFILE["name"])
```

## See Also
- [curator_agent.py](../agent/curator_agent.md)
- [email_agent.py](../agent/email_agent.md)
