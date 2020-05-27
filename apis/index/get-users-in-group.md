---
description: Get users in a group
---

# GET-users-in-group

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/users/in-group/:groupId" %}
{% api-method-summary %}
Get users in a group
{% endapi-method-summary %}

{% api-method-description %}
Retrieve all users in a group.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="groupId" type="number" required=true %}
Group Id
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
        "id": 1,
        "username": "cypress",
        "firstName": "xxxxx",
        "lastName": "yyyyyy",
        "email": "xxx@gmail.com",
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
            },
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
            }
        ]
    },
    {
        "id": 2,
        "username": "tmjee",
        "firstName": "toby",
        "lastName": "jee",
        "email": "tmjee1@gmail.com",
        "theme": "deeppurple_amber_dark",
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
            },
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
            }
        ]
    },
    {
        "id": 3,
        "username": "sxjee",
        "firstName": "song xian",
        "lastName": "jee",
        "email": "sxjee@gmail.com",
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
            },
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
            }
        ]
    },
    {
        "id": 49,
        "username": "invitation1",
        "firstName": "invitation1_firstName",
        "lastName": "invitation1_lastName",
        "email": "invitation1@gmail.com",
        "theme": "deeppurple_amber_light",
        "groups": [
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
            },
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
            }
        ]
    },
    {
        "id": 4,
        "username": "viewer1",
        "firstName": "viewer1_firstname",
        "lastName": "viewer1_lastname",
        "email": "viewer1@gmail.com",
        "theme": "pink_bluegrey_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 9,
        "username": "viewer2",
        "firstName": "viewer2_firstname",
        "lastName": "viewer2_lastname",
        "email": "viewer2@gmail.com",
        "theme": "indigo_pink_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 14,
        "username": "viewer3",
        "firstName": "viewer3_firstname",
        "lastName": "viewer3_lastname",
        "email": "viewer3@gmail.com",
        "theme": "deeppurple_amber_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 19,
        "username": "viewer4",
        "firstName": "viewer4_firstname",
        "lastName": "viewer4_lastname",
        "email": "viewer4@gmail.com",
        "theme": "indigo_lightblue_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 24,
        "username": "viewer5",
        "firstName": "viewer5_firstname",
        "lastName": "viewer5_lastname",
        "email": "viewer5@gmail.com",
        "theme": "purple_green_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 29,
        "username": "viewer6",
        "firstName": "viewer6_firstname",
        "lastName": "viewer6_lastname",
        "email": "viewer6@gmail.com",
        "theme": "pink_bluegrey_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 34,
        "username": "viewer7",
        "firstName": "viewer7_firstname",
        "lastName": "viewer7_lastname",
        "email": "viewer7@gmail.com",
        "theme": "indigo_pink_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 39,
        "username": "viewer8",
        "firstName": "viewer8_firstname",
        "lastName": "viewer8_lastname",
        "email": "viewer8@gmail.com",
        "theme": "deeppurple_amber_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 44,
        "username": "viewer9",
        "firstName": "viewer9_firstname",
        "lastName": "viewer9_lastname",
        "email": "viewer9@gmail.com",
        "theme": "indigo_lightblue_dark",
        "groups": [
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



