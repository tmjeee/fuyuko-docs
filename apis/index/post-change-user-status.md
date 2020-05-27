---
description: Change user's status
---

# POST-change-user-status

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/user/:userId/status/:status" %}
{% api-method-summary %}
Change user's status
{% endapi-method-summary %}

{% api-method-description %}
Change user's status.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userId" type="number" required=false %}
User Id
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" %}
Status code.
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
{
    "status": "SUCCESS",
    "message": "User 2 status altered (ENABLED)"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



