---
description: Schedule Validation
---

# POST-schedule-validation

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/validation" %}
{% api-method-summary %}
Schedule validation
{% endapi-method-summary %}

{% api-method-description %}
Schedule a validation job run.
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
Authentication tokens.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="description" type="string" required=false %}
Description given to this validation
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=true %}
Name of validation given
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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
    "ok": true,
    "validationId": 2
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



