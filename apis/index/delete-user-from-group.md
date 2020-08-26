---
description: Delete user from group
---

# DELETE-user-from-group

{% api-method method="delete" host="https://<host>:<port>/api/v1" path="/group/:groupId/remove-user/:userId" %}
{% api-method-summary %}
Delete user from group
{% endapi-method-summary %}

{% api-method-description %}
Delete user from group.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="groupId" type="number" required=true %}
Group Id
{% endapi-method-parameter %}

{% api-method-parameter name="userId" type="number" required=true %}
User Id.
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
    "message": "User 50 deleted from group 1"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



