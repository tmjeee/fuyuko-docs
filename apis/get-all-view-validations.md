---
description: Get all views' validations
---

# GET-all-view-validations

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/validations" %}
{% api-method-summary %}
Get all views' validations
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" %}
View ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication tokens.
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
        "name": "test view1 vaslidation",
        "description": "asdsdsd",
        "progress": "COMPLETED",
        "viewId": 1,
        "creationDate": "2020-03-25T13:42:20.000Z",
        "lastUpdate": "2020-03-25T13:42:22.000Z"
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



