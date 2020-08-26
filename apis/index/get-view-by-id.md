---
description: Get view by id
---

# GET-view-by-id

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId" %}
{% api-method-summary %}
Get view by id
{% endapi-method-summary %}

{% api-method-description %}
Get View by id.
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
Successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
  "payload": {
    "id": 1,
    "name": "Test View 1",
    "description": "Test View 1 Description",
    "creationDate": "2020-03-23T06:51:24.000Z",
    "lastUpdate": "2020-03-23T06:51:24.000Z"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



