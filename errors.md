# Error Handling

When an API request fails, the NG Mushrooms API returns a standard HTTP error response code along with a JSON message explaining what went wrong.

---

### Common Status Codes

| Status Code | Description | Reason |
| :--- | :--- | :--- |
| `400 Bad Request` | Invalid Input | Missing a required field in the request. |
| `401 Unauthorized` | Invalid API Key | The security pass provided is wrong or expired. |
| `404 Not Found` | Resource Missing | The endpoint URL or item does not exist. |

---

### Example Error Response (401 Unauthorized)

```json
{
  "error": "unauthorized",
  "message": "The provided API key is invalid or has been revoked."
}