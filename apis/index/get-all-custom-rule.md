---
description: Get all custom rules
---

# GET-all-custom-rules

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/custom-rules" %}
{% api-method-summary %}
Get all custom rules
{% endapi-method-summary %}

{% api-method-description %}
Get all custom rules.
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
Ssuccessfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
  "payload": [
    {
        "id": 1,
        "name": "0.0.1-sample-rule-1.js",
        "description": "0.0.1 Sample Rule #1"
    },
    {
        "id": 2,
        "name": "0.0.2-sample-rule-2.js",
        "description": "0.0.2 Sample Rule #2"
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



