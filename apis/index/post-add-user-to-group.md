---
description: Add user to a group
---

# POST-add-user-to-group

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/group/:groupId/add-user/:userId" %}
{% api-method-summary %}
Add user to a group
{% endapi-method-summary %}

{% api-method-description %}
Add user to group.
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
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "User 50 added to group 1"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



