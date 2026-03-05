# email.py Documentation

## Overview
Implements email sending and formatting utilities for the AI News Aggregator, including markdown-to-HTML conversion and email delivery via SMTP.

## Functions
### send_email(subject: str, body_text: str, body_html: str = None, recipients: list = None)
Sends an email with the given subject and body to the specified recipients using Gmail SMTP.

### markdown_to_html(markdown_text: str) -> str
Converts markdown text to styled HTML for email content.

### digest_to_html(digest_response) -> str
Converts an EmailDigestResponse object to HTML for email delivery.

### send_email_to_self(subject: str, body: str)
Sends an email to the configured user email address.

## Environment Variables
- **MY_EMAIL**: Sender and default recipient email address
- **APP_PASSWORD**: Gmail app password

## Usage Example
```python
from app.services.email import send_email, markdown_to_html
digest_html = markdown_to_html(markdown_text)
send_email(subject, body_text, body_html)
```

## See Also
- [process_email.py](process_email.md)
