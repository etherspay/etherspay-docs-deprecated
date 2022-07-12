---
description: https://api.etherspay.com
---

# Authentication

The etherspay REST API uses API keys to authenticate requests. You can view and manage your API keys in your [<mark style="color:green;">project</mark> ](https://etherspay.com/dashboard)<mark style="color:green;">settings</mark>.

{% hint style="warning" %}
Do not share your api key with anyone!
{% endhint %}

All API requests must be made over [HTTPS](http://en.wikipedia.org/wiki/HTTP\_Secure). Calls made over plain HTTP will fail. API requests without authentication will also fail.

Insert your project secret in the **x-api-key** header.

{% tabs %}
{% tab title="cURL" %}
```bash
curl -X GET http://localhost:5000/v1 \
    -H "x-api-key: 15a49de6-6c90-495f-9c35-85ea89ebf5a8"
```
{% endtab %}

{% tab title="Node.js" %}
```javascript
const Etherspay = require('etherspay');
const etp = new Etherspay('15a49de6-6c90-495f-9c35-85ea89ebf5a8'); // Insert your project key here
```
{% endtab %}
{% endtabs %}
