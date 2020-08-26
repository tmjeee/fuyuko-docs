# GET-groups-not-associated-with-pricing-structure

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/pricing-structure-group-associations" %}
{% api-method-summary %}
Get groups not associated with pricing structure
{% endapi-method-summary %}

{% api-method-description %}
Get pricing structures and groups linked to each of those pricing structures.
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
Successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "Retrieved successfully",
    "payload": [
        {
            "pricingStructure": {
                "id": 1,
                "name": "Pricing Structure #1",
                "description": "Pricing Structure #1 Description",
                "viewId": 1,
                "viewName": "Test View 1",
                "lastUpdate": "2020-05-01T02:32:39.000Z",
                "creationDate": "2020-05-01T02:32:39.000Z"
            },
            "groups": [
                {
                    "id": 3,
                    "name": "ADMIN Group",
                    "isSystem": 1,
                    "description": "Group with VIEW & EDIT & PARTNER & ADMIN roles",
                    "status": "ENABLED",
                    "roles": [
                        {
                            "id": 1,
                            "name": "VIEW",
                            "description": "VIEW Role"
                        },
                        {
                            "id": 2,
                            "name": "EDIT",
                            "description": "EDIT Role"
                        },
                        {
                            "id": 3,
                            "name": "ADMIN",
                            "description": "ADMIN Role"
                        },
                        {
                            "id": 4,
                            "name": "PARTNER",
                            "description": "PARTNER Role"
                        }
                    ]
                },
                {
                    "id": 4,
                    "name": "PARTNER Group",
                    "isSystem": 1,
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
            "pricingStructure": {
                "id": 2,
                "name": "Pricing Structure #2",
                "description": "Pricing Structure #2 Description",
                "viewId": 1,
                "viewName": "Test View 1",
                "lastUpdate": "2020-05-01T02:32:39.000Z",
                "creationDate": "2020-05-01T02:32:39.000Z"
            },
            "groups": [
                {
                    "id": 3,
                    "name": "ADMIN Group",
                    "isSystem": 1,
                    "description": "Group with VIEW & EDIT & PARTNER & ADMIN roles",
                    "status": "ENABLED",
                    "roles": [
                        {
                            "id": 1,
                            "name": "VIEW",
                            "description": "VIEW Role"
                        },
                        {
                            "id": 2,
                            "name": "EDIT",
                            "description": "EDIT Role"
                        },
                        {
                            "id": 3,
                            "name": "ADMIN",
                            "description": "ADMIN Role"
                        },
                        {
                            "id": 4,
                            "name": "PARTNER",
                            "description": "PARTNER Role"
                        }
                    ]
                },
                {
                    "id": 4,
                    "name": "PARTNER Group",
                    "isSystem": 1,
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
            "pricingStructure": {
                "id": 3,
                "name": "Pricing Structure #1",
                "description": "Pricing Structure #1 Description",
                "viewId": 2,
                "viewName": "Test View 2",
                "lastUpdate": "2020-05-01T02:32:39.000Z",
                "creationDate": "2020-05-01T02:32:39.000Z"
            },
            "groups": [
                {
                    "id": 3,
                    "name": "ADMIN Group",
                    "isSystem": 1,
                    "description": "Group with VIEW & EDIT & PARTNER & ADMIN roles",
                    "status": "ENABLED",
                    "roles": [
                        {
                            "id": 1,
                            "name": "VIEW",
                            "description": "VIEW Role"
                        },
                        {
                            "id": 2,
                            "name": "EDIT",
                            "description": "EDIT Role"
                        },
                        {
                            "id": 3,
                            "name": "ADMIN",
                            "description": "ADMIN Role"
                        },
                        {
                            "id": 4,
                            "name": "PARTNER",
                            "description": "PARTNER Role"
                        }
                    ]
                },
                {
                    "id": 4,
                    "name": "PARTNER Group",
                    "isSystem": 1,
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
            "pricingStructure": {
                "id": 4,
                "name": "Pricing Structure #2",
                "description": "Pricing Structure #2 Description",
                "viewId": 2,
                "viewName": "Test View 2",
                "lastUpdate": "2020-05-01T02:32:39.000Z",
                "creationDate": "2020-05-01T02:32:39.000Z"
            },
            "groups": [
                {
                    "id": 3,
                    "name": "ADMIN Group",
                    "isSystem": 1,
                    "description": "Group with VIEW & EDIT & PARTNER & ADMIN roles",
                    "status": "ENABLED",
                    "roles": [
                        {
                            "id": 1,
                            "name": "VIEW",
                            "description": "VIEW Role"
                        },
                        {
                            "id": 2,
                            "name": "EDIT",
                            "description": "EDIT Role"
                        },
                        {
                            "id": 3,
                            "name": "ADMIN",
                            "description": "ADMIN Role"
                        },
                        {
                            "id": 4,
                            "name": "PARTNER",
                            "description": "PARTNER Role"
                        }
                    ]
                },
                {
                    "id": 4,
                    "name": "PARTNER Group",
                    "isSystem": 1,
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



