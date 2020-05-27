---
description: Get all pricing structures
---

# GET-all-pricing-stuctures

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/pricingStructures" %}
{% api-method-summary %}
Get all pricing structures
{% endapi-method-summary %}

{% api-method-description %}
Get all pricing structures.
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
        "name": "Pricing Structure #1",
        "viewId": 1,
        "description": "Pricing Structure #1 Description"
    },
    {
        "id": 2,
        "name": "Pricing Structure #2",
        "viewId": 2,
        "description": "Pricing Structure #2 Description"
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



