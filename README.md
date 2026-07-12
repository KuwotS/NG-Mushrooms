# NG Mushrooms API 
Welcome to the official API documentation for **NG Mushrooms**! This reference guide provides developers with the endpoints and integration workflows required to manage organic mushroom inventory, track stock variations, and process orders programmatically. 
---
### Key Capabilities 

* **Inventory Tracking:** Query live stock levels for fresh and dried variations.
* **Real-time Status Updates:** Monitor product availablility dynamically to prevent order backlogs.
* **Localization Native:** Built natively to handle currency requirements in Nigerian Naira (NGN).
---
### Getting Started 

To begin integrating with the NG Mushrooms API, follow this quick 3-step workflow to make your first authorized request.

#### Step 1: Secure Your API Key
Before making any requests, you must obtain a unique security token. Head over to the [Authentication](authentication.md) page to learn how to generate your sandbox key and pass it securely in your request headers.

#### Step 2: Review Rate Limits and Error Codes
To ensure your application doesn't get temporarily blocked, check the [Rate Limiting](rate-limiting.md) guidelines. If you run into any validation issues while testing, consult the [Error Handling](errors.md) guide for standard status code definitions.

#### Step 3: Fetch Live Inventory Data
Once your authentication header is set up, make a `GET` request to our inventory endpoint to retrieve real-time stock levels and pricing:

```bash
GET https://api.ngmushrooms.com/v1/inventory
```

---

### Localization

* **Language:** The text responses are written in **English**.
* **Currency:** The prices will always display in **Nigerian Naira (NGN)**. 