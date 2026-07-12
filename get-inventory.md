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
  "business_name": "Nagari Mushrooms",
  "currency": "NGN",
  "in_stock": true,
  "variations": [
    {
      "type": "Fresh Oyster",
      "weight_kg": 50,
      "price_per_kg": 3500
    },
    {
      "type": "Dried Shiitake",
      "weight_kg": 12,
      "price_per_kg": 8500
    }
  ]
}
--- 