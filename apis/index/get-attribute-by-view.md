---
description: Get attribute by view
---

# GET-attribute-by-view

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/attribute/:attributeId/view/:viewId" %}
{% api-method-summary %}
Get attribute by view
{% endapi-method-summary %}

{% api-method-description %}
Get attributes in a view.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
{% endapi-method-parameter %}

{% api-method-parameter name="attributeId" type="number" required=true %}
Attribute Id
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
{
  "status": "SUCCESS",
  "message": "....",
  "payload": {
    "id": 1,
    "name": "string attribute",
    "description": "string attribute description",
    "type": "string",
    "creationDate": "2020-03-23T06:51:24.000Z",
    "lastUpdate": "2020-03-23T06:51:24.000Z"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



