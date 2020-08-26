---
description: Find groups that have no role provided
---

# GET-search-group-with-no-such-role

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/groups/no-role/:roleName/:groupName" %}
{% api-method-summary %}
Get groups with no roles given
{% endapi-method-summary %}

{% api-method-description %}
Search for group that do not have the given role-name by group name.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="roleName" type="string" required=true %}
Role name
{% endapi-method-parameter %}

{% api-method-parameter name="groupName" type="string" required=false %}
Group name \(wild card acceptable\)
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token
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
    "message": ".....",
    "total": 1,
    "limit": 1,
    "offset": 0,
    "payload": [
        {
            "id": 2,
            "name": "EDIT Group",
            "description": "Group with VIEW & EDIT role",
            "status": "ENABLED",
            "roles": [
                {
                    "id": 2,
                    "name": "EDIT",
                    "description": "EDIT Role"
                }
            ]
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



