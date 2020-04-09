---
description: Get invitations by code
---

# GET-inviations-by-code

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/invitations/:code" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="code" type="string" required=true %}
Invitation code
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
  "payload": {
    "id": 3,
    "activated": 0,
    "creationDate": "2020-03-09T23:04:14.000Z",
    "email": "invitation3@gmail.com",
    "groupIds": [
        1,
        4
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



