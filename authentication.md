# Authentication

---
### Obtaining Your API Key

To get your API credentials:
1. Log into your **NG Mushrooms** developer portal account.
2. Navigate to **Settings > API Keys**. 
3. Click **Generate New Token** and copy your secret key immediately.

> **Security Notice:** Treat your API Key like a password. Never share it publicly or commit it to GitHub repositories. 
---
### Implementation Example
Your API Key must be included in the **Header** of every HTTP request using the `X-API-Key` parameter.

Here is what an authenticated header setup looks like:

```json
{
    "Content-Type": "application/json",
    "X-API-Key": "ng_shroom_secret_live_99x"
}