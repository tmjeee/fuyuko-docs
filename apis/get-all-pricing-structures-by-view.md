---
description: Get all pricing structures by view
---

# GET-all-pricing-structures-by-view

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/pricingStructures/view/:viewId" %}
{% api-method-summary %}
Get all pricing structures by view
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View ID
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
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
[
    {
        "id": 1,
        "viewId": 1,
        "name": "Pricing Structure #1",
        "description": "Pricing Structure #1 Description",
        "creationDate": "2020-03-23T06:51:24.000Z",
        "lastUpdate": "2020-03-23T06:51:24.000Z"
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



