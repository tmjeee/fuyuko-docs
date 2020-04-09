---
description: Get all roles
---

# GET-all-roles

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/roles" %}
{% api-method-summary %}
Get all roles
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
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
  "payload": [
    {
        "id": 1,
        "name": "VIEW",
        "description": "VIEW Role"
    },
    {
        "id": 2,
        "name": "EDIT",
        "description": "EDIT Role"
    },
    {
        "id": 3,
        "name": "ADMIN",
        "description": "ADMIN Role"
    },
    {
        "id": 4,
        "name": "PARTNER",
        "description": "PARTNER Role"
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



