---
description: https://api.etherspay.com
---

# Authentication

The etherspay REST API uses API keys to authenticate requests. You can view and manage your API keys in [<mark style="color:green;">the Etherspay Dashboard</mark>](https://dashboard.etherspay.com).

Test mode secret keys have the prefix `ep_test` and live mode secret keys have the prefix `ep_live`

{% hint style="warning" %}
Do not share your api key with anyone!
{% endhint %}

All API requests must be made over [HTTPS](http://en.wikipedia.org/wiki/HTTP\_Secure). Calls made over plain HTTP will fail. API requests without authentication will also fail.
