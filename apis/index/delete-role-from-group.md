---
description: Delete a role from a group
---

# DELETE-role-from-group

{% api-method method="delete" host="https://<host>:<port>/api/v1" path="/group/:groupId/role/:roleName" %}
{% api-method-summary %}
Delete role from group
{% endapi-method-summary %}

{% api-method-description %}
Remove role from a group.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="groupId" type="string" required=true %}
Group Id
{% endapi-method-parameter %}

{% api-method-parameter name="roleName" type="string" required=true %}
Role name
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
    "message": "Role VIEW deleted from group 1"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



