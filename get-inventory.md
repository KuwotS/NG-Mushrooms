# Get Mushroom Inventory

Use this endpoint to retrieve a list of all organic mushrooms in the warehouse, including stock status and currency pricing.

### HTTP Request 

`GET https://api.ngmushrooms.com./v1/inventory`
---
### Response Parameters 

When you make a successful call to the endpoint, the server will return a JSON object with the following fields:

* **business_name** (string): The registered name of the supplier.
* **currency**(string): The currency code used for pricing, which defaults to `NGN`.
* **in_stock** (boolean): Indicates if the items are physically available (`true` or `false`). 
---
### Example Response (200 OK)

```json
{
    "business_name": "NG Mushrooms",
    "currency": "NG",
    "in_stock": true
}
--- 