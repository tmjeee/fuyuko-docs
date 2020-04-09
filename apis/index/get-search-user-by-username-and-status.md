---
description: Search user by username and status
---

# GET-search-user-by-username-and-status

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/search/status/:status/user/:username" %}
{% api-method-summary %}
Search user by status and / or username
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="status" type="string" required=true %}
status
{% endapi-method-parameter %}

{% api-method-parameter name="username" type="string" %}
Username to search for
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
  "message": "....",
  "payload": [
    {
        "id": 1,
        "username": "cypress",
        "firstName": "cypress",
        "lastName": "jee",
        "email": "tmjeee@gmail.com",
        "theme": "deeppurple_amber_light",
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
    },
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
    },
    {
        "id": 6,
        "username": "admin1",
        "firstName": "admin1_firstname",
        "lastName": "admin1_lastname",
        "email": "admin1@gmail.com",
        "theme": "indigo_lightblue_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 11,
        "username": "admin2",
        "firstName": "admin2_firstname",
        "lastName": "admin2_lastname",
        "email": "admin2@gmail.com",
        "theme": "purple_green_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 16,
        "username": "admin3",
        "firstName": "admin3_firstname",
        "lastName": "admin3_lastname",
        "email": "admin3@gmail.com",
        "theme": "pink_bluegrey_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 21,
        "username": "admin4",
        "firstName": "admin4_firstname",
        "lastName": "admin4_lastname",
        "email": "admin4@gmail.com",
        "theme": "indigo_pink_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 26,
        "username": "admin5",
        "firstName": "admin5_firstname",
        "lastName": "admin5_lastname",
        "email": "admin5@gmail.com",
        "theme": "deeppurple_amber_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 31,
        "username": "admin6",
        "firstName": "admin6_firstname",
        "lastName": "admin6_lastname",
        "email": "admin6@gmail.com",
        "theme": "indigo_lightblue_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 36,
        "username": "admin7",
        "firstName": "admin7_firstname",
        "lastName": "admin7_lastname",
        "email": "admin7@gmail.com",
        "theme": "purple_green_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 41,
        "username": "admin8",
        "firstName": "admin8_firstname",
        "lastName": "admin8_lastname",
        "email": "admin8@gmail.com",
        "theme": "pink_bluegrey_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 46,
        "username": "admin9",
        "firstName": "admin9_firstname",
        "lastName": "admin9_lastname",
        "email": "admin9@gmail.com",
        "theme": "indigo_pink_dark",
        "groups": [
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
            }
        ]
    },
    {
        "id": 7,
        "username": "partner1",
        "firstName": "partner1_firstname",
        "lastName": "partner1_lastname",
        "email": "partner1@gmail.com",
        "theme": "indigo_pink_light",
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
            }
        ]
    },
    {
        "id": 12,
        "username": "partner2",
        "firstName": "partner2_firstname",
        "lastName": "partner2_lastname",
        "email": "partner2@gmail.com",
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
            }
        ]
    },
    {
        "id": 17,
        "username": "partner3",
        "firstName": "partner3_firstname",
        "lastName": "partner3_lastname",
        "email": "partner3@gmail.com",
        "theme": "indigo_lightblue_light",
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
            }
        ]
    },
    {
        "id": 22,
        "username": "partner4",
        "firstName": "partner4_firstname",
        "lastName": "partner4_lastname",
        "email": "partner4@gmail.com",
        "theme": "purple_green_light",
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
            }
        ]
    },
    {
        "id": 27,
        "username": "partner5",
        "firstName": "partner5_firstname",
        "lastName": "partner5_lastname",
        "email": "partner5@gmail.com",
        "theme": "pink_bluegrey_light",
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
            }
        ]
    },
    {
        "id": 32,
        "username": "partner6",
        "firstName": "partner6_firstname",
        "lastName": "partner6_lastname",
        "email": "partner6@gmail.com",
        "theme": "indigo_pink_light",
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
            }
        ]
    },
    {
        "id": 37,
        "username": "partner7",
        "firstName": "partner7_firstname",
        "lastName": "partner7_lastname",
        "email": "partner7@gmail.com",
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
            }
        ]
    },
    {
        "id": 42,
        "username": "partner8",
        "firstName": "partner8_firstname",
        "lastName": "partner8_lastname",
        "email": "partner8@gmail.com",
        "theme": "indigo_lightblue_light",
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
            }
        ]
    },
    {
        "id": 47,
        "username": "partner9",
        "firstName": "partner9_firstname",
        "lastName": "partner9_lastname",
        "email": "partner9@gmail.com",
        "theme": "purple_green_light",
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



