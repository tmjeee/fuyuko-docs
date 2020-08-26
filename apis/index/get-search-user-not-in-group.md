---
description: Search for users not in group
---

# GET-search-user-not-in-group

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/users/not-in-group/:groupId/:username" %}
{% api-method-summary %}
Search forusers not in group
{% endapi-method-summary %}

{% api-method-description %}
Search for users not in group by username.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="groupId" type="number" required=true %}
Group id
{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" %}
Username
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
  "message": "....",
  "payload": [
    {
        "id": 5,
        "username": "editor1",
        "firstName": "editor1_firstname",
        "lastName": "editor1_lastname",
        "email": "editor1@gmail.com",
        "theme": "indigo_lightblue_light",
        "groups": [
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
    },
    {
        "id": 10,
        "username": "editor2",
        "firstName": "editor2_firstname",
        "lastName": "editor2_lastname",
        "email": "editor2@gmail.com",
        "theme": "purple_green_light",
        "groups": [
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
    },
    {
        "id": 15,
        "username": "editor3",
        "firstName": "editor3_firstname",
        "lastName": "editor3_lastname",
        "email": "editor3@gmail.com",
        "theme": "pink_bluegrey_light",
        "groups": [
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
    },
    {
        "id": 20,
        "username": "editor4",
        "firstName": "editor4_firstname",
        "lastName": "editor4_lastname",
        "email": "editor4@gmail.com",
        "theme": "indigo_pink_light",
        "groups": [
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
    },
    {
        "id": 25,
        "username": "editor5",
        "firstName": "editor5_firstname",
        "lastName": "editor5_lastname",
        "email": "editor5@gmail.com",
        "theme": "deeppurple_amber_light",
        "groups": [
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
    },
    {
        "id": 30,
        "username": "editor6",
        "firstName": "editor6_firstname",
        "lastName": "editor6_lastname",
        "email": "editor6@gmail.com",
        "theme": "indigo_lightblue_light",
        "groups": [
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
    },
    {
        "id": 35,
        "username": "editor7",
        "firstName": "editor7_firstname",
        "lastName": "editor7_lastname",
        "email": "editor7@gmail.com",
        "theme": "purple_green_light",
        "groups": [
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
    },
    {
        "id": 40,
        "username": "editor8",
        "firstName": "editor8_firstname",
        "lastName": "editor8_lastname",
        "email": "editor8@gmail.com",
        "theme": "pink_bluegrey_light",
        "groups": [
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
    },
    {
        "id": 45,
        "username": "editor9",
        "firstName": "editor9_firstname",
        "lastName": "editor9_lastname",
        "email": "editor9@gmail.com",
        "theme": "indigo_pink_light",
        "groups": [
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
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



