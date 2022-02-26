---
description: https://api.etherspay.com
---

# Error handling

The etherspay REST API will return conventional HTTP status codes to indicate the success or failure of an API request. You can use these codes to handle errors in your application.

These are the most common codes returned by the etherspay API.

| Codes                              | Explanation                                                              |
| ---------------------------------- | ------------------------------------------------------------------------ |
| 200 - OK                           | Everything worked as expected.                                           |
| 400 - Bad Request                  | The request was unacceptable, often due to missing a required parameter. |
| 401 - Unauthorized                 | No valid API key provided.                                               |
| 402 - Request failed               | The parameters were valid but the request failed.                        |
| 403 - Forbidden                    | The API key doesn't have permissions to perform the request.             |
| 404 - Not found                    | The requested resource doesn't exist.                                    |
| 409 - Conflict                     | The request conflicts with another request                               |
| 429 - Too Many Requests            | Too many requests hit the API too quickly.                               |
| 500, 502, 503, 504 - Server Errors | Something went wrong on Etherspay's end.                                 |
