---
description: https://api.etherspay.com
---

# Promotion Codes

A Promotion Code represents a customer-redeemable code.

<details>

<summary>Endpoints</summary>

<mark style="color:green;">**POST**</mark>       _/v1/promotion\_codes_

<mark style="color:orange;">**UPDATE**</mark>   _/v1/promotion\_codes/:id_

<mark style="color:blue;">**GET**</mark>          _/v1/promotion\_codes/:id_

<mark style="color:blue;">**GET**</mark>          _/v1/promotion\_codes_

<mark style="color:red;">**DELETE**</mark>    _/v1/promotion\_codes/:id_

</details>

### Promotion code object

```json
{
  "id": "cl5n2ssco00048osj9szvjzk7",
  "name": "PROMO",
  "code": "Y13",
  "active": true,
  "amount_off": null,
  "created_at": 1657926782,
  "first_time_transaction": false,
  "max_redemptions": null,
  "min_amount": null,
  "percent_off": null
  "projectId": "cl5n2go7e00800csjh3tv6k8x",
}
```

### Integration

{% tabs %}
{% tab title="cURL" %}
```bash
curl https://api.etherspay.com/v1/promotion_codes \
  -u sk_test_51JMIa9DARRNpGJZ7JrU8HfeKO1Ckkvl6e4svRLiHl3GsUZBX1FJgZEOrIY5BVMVnoXabwJVEhebYiOcUeS2AHh1X004xbHVPeM: \
  -d coupon=Z4OV52SU
```
{% endtab %}

{% tab title="Node.js" %}
```javascript
const stripe = require('stripe')('sk_test_51JMIa9DARRNpGJZ7JrU8HfeKO1Ckkvl6e4svRLiHl3GsUZBX1FJgZEOrIY5BVMVnoXabwJVEhebYiOcUeS2AHh1X004xbHVPeM');

const promotionCode = await etp.promotioncodes.create({
  name: 'My code', // Required
  code: 'Z4OV52SU', // Required
  // Other params (see above)
});
```
{% endtab %}
{% endtabs %}
