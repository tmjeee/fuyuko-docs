---
description: Search for group by name
---

# GET-search-for-group-by-name

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/group/:groupName/search" %}
{% api-method-summary %}
Search for group by name
{% endapi-method-summary %}

{% api-method-description %}
Search groups by name.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="groupName" type="string" required=true %}
Group name
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
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
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

{% hint style="info" %}
`groupName` path parameter is text to be search eg. `view` will matched `view group` and `group for view` etc
{% endhint %}

