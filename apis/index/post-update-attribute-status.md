---
description: Update attribute status
---

# POST-change-attribute-status

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/attribute/:attributeId/state/:state" %}
{% api-method-summary %}
Change attribute status
{% endapi-method-summary %}

{% api-method-description %}
Update an attribute status.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="attributeId" type="number" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="state" type="string" required=true %}
State code.
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
Successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "Attribute 1 deleted"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



