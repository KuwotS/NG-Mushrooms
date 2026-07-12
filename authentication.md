# Authentication

The NG Mushrooms API uses API keys to authenticate incoming requests. Your API keys carry significant privileges, so please keep them secure and never share them in publicly accessible code spaces (like client-side browser files).

---

### Authentication Protocol

All API requests must be made over HTTPS. Requests sent over unencrypted HTTP will automatically fail. 

We use the standard **Bearer Token** authentication protocol. You must pass your unique API key inside the HTTP `Authorization` header of every request.

---

### Header Format

Configure your request headers using the following key-value structure:

| Header Key | Expected Value | Description |
| :--- | :--- | :--- |
| `Authorization` | `Bearer YOUR_API_KEY` | Replaces `YOUR_API_KEY` with your actual sandbox or production token. |
| `Content-Type` | `application/json` | Mandated for all write operations (`POST` requests). |

---

### Example Header Configuration

Here is how your request headers should look when making a call:

```http
GET /v1/inventory HTTP/1.1
Host: api.ngmushrooms.com
Authorization: Bearer ng_sandbox_771x99283
Content-Type: application/json
```

> Security Note: If the Authorization header is missing, malformed, or contains an invalid key, the API server will reject the request with a 401 Unauthorized status code.

