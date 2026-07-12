# Rate Limiting

To ensure system stability and fair usage across all users, the NG Mushrooms API enforces rate limits on all incoming requests.

---

### Limits by Tier

Rate limits are applied based on your API key subscription tier:

* **Sandbox Tier:** 60 requests per minute (Great for testing!)
* **Production Tier:** 1,000 requests per minute

---

### Rate Limit Headers

Every response from our server includes special HTTP headers to help you track your usage programmatically:

| Header | Description |
| :--- | :--- |
| `X-RateLimit-Limit` | The maximum number of requests allowed in a period. |
| `X-RateLimit-Remaining` | The number of requests you have left for the current window. |
| `X-RateLimit-Reset` | The time remaining (in seconds) until the limit resets. |

> 💡 **Pro-Tip:** If your application exceeds the limit, the API will return a `429 Too Many Requests` status code. Always build a slight delay into your code if you hit this limit.