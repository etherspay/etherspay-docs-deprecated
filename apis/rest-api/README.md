# REST API

The Etherspay REST API returns [<mark style="color:green;">JSON-encoded</mark>](http://www.json.org/) responses, and uses standard HTTP response codes, authentication, and verbs.

## API reference



The etherspay API is organized around [<mark style="color:green;">REST</mark>](http://en.wikipedia.org/wiki/Representational\_State\_Transfer). The API has predictable resource-oriented URLs, accepts [<mark style="color:green;">form-encoded</mark>](https://en.wikipedia.org/wiki/POST\_\(HTTP\)#Use\_for\_submitting\_web\_forms) request bodies, returns [<mark style="color:green;">JSON-encoded</mark>](http://www.json.org/) responses, and uses standard HTTP response codes, authentication, and verbs.

API Base URL

The API requires an authentication token to verify the user. Visit the [<mark style="color:green;">authentication</mark>](authentication.md) section for in depth information.

```
https://api.etherspay.com
```

{% hint style="success" %}
**Base url:** [<mark style="color:green;">**https://api.etherspay.com**</mark>](https://api.etherspay.com)<mark style="color:green;">****</mark>
{% endhint %}



### API status

To get the API status you can make a GET request to [<mark style="color:green;">https://api.etherspay.com/status</mark>](https://api.etherspay.com/status)<mark style="color:green;"></mark>

{% swagger method="get" path="/" baseUrl="https://api.etherspay.com/status" summary="Query API status" %}
{% swagger-description %}
No params needed
{% endswagger-description %}

{% swagger-response status="200: OK" description="This method will return the current server status." %}
```javascript
{
    "Server status": "Operational",
    "Code": 200,
}
```
{% endswagger-response %}
{% endswagger %}
