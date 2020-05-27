---
description: Get all groups
---

# GET-all-groups

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/groups" %}
{% api-method-summary %}
Get all groups
{% endapi-method-summary %}

{% api-method-description %}
Get all groups.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
    "message": "....",
    "total": 4,
    "limit": 4,
    "offset": 0,
    "payload": [
        {
            "id": 1,
            "name": "VIEW Group",
            "description": "Group with VIEW role",
            "status": "ENABLED",
            "roles": [
                {
                    "id": 1,
                    "name": "VIEW",
                    "description": "VIEW Role"
                }
            ]
        },
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
        },
        {
            "id": 3,
            "name": "ADMIN Group",
            "description": "Group with VIEW & EDIT & PARTNER & ADMIN role",
            "status": "ENABLED",
            "roles": [
                {
                    "id": 3,
                    "name": "ADMIN",
                    "description": "ADMIN Role"
                }
            ]
        },
        {
            "id": 4,
            "name": "PARTNER Group",
            "description": "Group with PARTNER role",
            "status": "ENABLED",
            "roles": [
                {
                    "id": 4,
                    "name": "PARTNER",
                    "description": "PARTNER Role"
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



