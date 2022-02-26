---
description: https://api.etherspay.com
---

# Invoices

### Fetching invoices

You can fetch all invoices created by your account using the following method.

{% swagger method="get" path="/" baseUrl="https://api.etherspay.com/invoices" summary="Fetching invoices" %}
{% swagger-description %}
To fetch all invoices leave the id parameter blank.
{% endswagger-description %}

{% swagger-parameter in="path" name="id" type="String" %}
Only fetch one specific payment (Optional)
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="Returns all payments within a json object" %}
```javascript
{
  "id": "ch_3Jz3y52eZvKYlo2C0MlUGqj9",
  "object": "charge",
  "customer": {
    "id": "cu_19yUkG2eZvKYlo2CJTFh2ZVA",
    "object": "customer",
    ...
  },
  "invoice": {
    "id": "in_1Jz3y62eZvKYlo2CtEM2LwJa",
    "object": "invoice",
    "subscription": {
      "id": "su_1Jf06h2eZvKYlo2C4Pq8zSWv",
      "object": "subscription",
      ...
    },
    ...
  },
  ...
}
```
{% endswagger-response %}
{% endswagger %}
