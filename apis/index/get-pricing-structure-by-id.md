---
description: Get pricing structure by id
---

# GET-pricing-structure-by-id

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/pricingStructure/:pricingStructureId" %}
{% api-method-summary %}
Get pricing structure by id
{% endapi-method-summary %}

{% api-method-description %}
Get pricing structure details by id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="pricingStructureId" type="number" required=true %}
ID of the cake to get, for free of course.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
  "payload": {
    "id": 1,
    "viewId": 1,
    "name": "Pricing Structure #1",
    "description": "Pricing Structure #1 Description",
    "creationDate": "2020-03-23T06:51:24.000Z",
    "lastUpdate": "2020-03-23T06:51:24.000Z"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



