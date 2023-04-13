---
description: https://etherspay.com
---

# Coupons

A Promotion Code represents a customer-redeemable code.

## Create a coupon

You can also manage your coupons in the project dashboard.

{% swagger method="post" path="coupons" baseUrl="https://api.etherspay.com/v1/" summary="Coupon creation is accessible via the API." %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="amount_off" type="Number" %}
A positive integer representing the amount to subtract from an invoice total (required if 

`percent_off`

 is not passed).
{% endswagger-parameter %}

{% swagger-parameter in="body" name="percent_off" type="Number" %}
A positive float larger than 0, and smaller or equal to 100, that represents the discount the coupon will apply (required if 

`amount_off`

 is not passed).
{% endswagger-parameter %}

{% swagger-parameter in="body" name="permanent" type="Boolean" %}
If set to 

`true`

 , the coupon code can be used on every transaction, unless manually disabled. When set to 

`false`

 , the coupon is only valid for a single transaction.
{% endswagger-parameter %}

{% swagger-response status="201: Created" description="Coupon created" %}
Returns a coupon object

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
{% endswagger-response %}
{% endswagger %}

### Integration

{% tabs %}
{% tab title="cURL" %}
```bash
curl https://api.etherspay.com/v1/coupons \
  -u sk_test_51JMIa9DARRNpGJZ7JrU8HfeKO1Ckkvl6e4svRLiHl3GsUZBX1FJgZEOrIY5BVMVnoXabwJVEhebYiOcUeS2AHh1X004xbHVPeM: \
  -d coupon=Z4OV52SU
```
{% endtab %}

{% tab title="Node.js" %}
```javascript
const stripe = require('stripe')('sk_test_51JMIa9DARRNpGJZ7JrU8HfeKO1Ckkvl6e4svRLiHl3GsUZBX1FJgZEOrIY5BVMVnoXabwJVEhebYiOcUeS2AHh1X004xbHVPeM');

const promotionCode = await etp.coupons.create({
  name: 'My code', // Required
  code: 'Z4OV52SU', // Required
  // Other params (see above)
});
```
{% endtab %}
{% endtabs %}

## Retrieve a coupon

