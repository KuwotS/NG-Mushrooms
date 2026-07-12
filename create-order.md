# create order

This endpoint allows external applications to programmatically submit a new customer order for organic mushrooms.

### HTTP Request

`POST https://api.ngmushrooms.com/v1/orders`

### Request Body Parameters

When sending a `POST` request, you must include a JSON body with the following fields:

* **customer\_name** (string, required): The full name of the buyer.
* **mushroom\_type** (string, required): The specific variation (e.g., `Fresh Oyster` or `Dried Shiitake`).
* **quantity\_kg** (integer, required): The total weight ordered in kilograms.

### Example Request Body

```json
{
  "customer_name": "Gimbiya Sodangi",
  "mushroom_type": "Fresh Oyster",
  "quantity_kg": 5
}
```

### Example Response (201 Created)

When the order is successfully placed, the server will return a confirmation payload:

```json
{
  "order_id": "ORD-99281-NG",
  "status": "pending_payment",
  "message": "Order received successfully."
}
```
