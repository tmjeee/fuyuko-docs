---
description: Get all rules in view
---

# GET-all-rules-by-view

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/rules" %}
{% api-method-summary %}
Get all rules in view
{% endapi-method-summary %}

{% api-method-description %}
Get all rules in a view.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="string" required=true %}
View Id.
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
        "name": "Rule #1",
        "status": "ENABLED",
        "description": "Rule #1 Description",
        "validateClauses": [
            {
                "id": 1,
                "attributeId": 1,
                "attributeName": "string attribute",
                "attributeType": "string",
                "operator": "eq",
                "condition": [
                    {
                        "type": "string",
                        "value": "val string 1"
                    },
                    {
                        "type": "string",
                        "value": "val string 2"
                    }
                ]
            }
        ],
        "whenClauses": [
            {
                "id": 1,
                "attributeId": 2,
                "attributeName": "text attribute",
                "attributeType": "text",
                "operator": "not eq",
                "condition": [
                    {
                        "type": "text",
                        "value": "val text 1"
                    },
                    {
                        "type": "text",
                        "value": "val text 2"
                    }
                ]
            }
        ]
    },
    {
        "id": 2,
        "name": "Rule #2",
        "status": "ENABLED",
        "description": "Rule #2 Description",
        "validateClauses": [
            {
                "id": 2,
                "attributeId": 1,
                "attributeName": "string attribute",
                "attributeType": "string",
                "operator": "eq",
                "condition": [
                    {
                        "type": "string",
                        "value": "val string 1"
                    },
                    {
                        "type": "string",
                        "value": "val string 2"
                    }
                ]
            }
        ],
        "whenClauses": [
            {
                "id": 2,
                "attributeId": 2,
                "attributeName": "text attribute",
                "attributeType": "text",
                "operator": "not eq",
                "condition": [
                    {
                        "type": "text",
                        "value": "val text 1"
                    },
                    {
                        "type": "text",
                        "value": "val text 2"
                    }
                ]
            }
        ]
    },
    {
        "id": 3,
        "name": "Rule #3",
        "status": "ENABLED",
        "description": "Rule #3 Description",
        "validateClauses": [
            {
                "id": 3,
                "attributeId": 1,
                "attributeName": "string attribute",
                "attributeType": "string",
                "operator": "eq",
                "condition": [
                    {
                        "type": "string",
                        "value": "val string 1"
                    },
                    {
                        "type": "string",
                        "value": "val string 2"
                    }
                ]
            }
        ],
        "whenClauses": [
            {
                "id": 3,
                "attributeId": 2,
                "attributeName": "text attribute",
                "attributeType": "text",
                "operator": "not eq",
                "condition": [
                    {
                        "type": "text",
                        "value": "val text 1"
                    },
                    {
                        "type": "text",
                        "value": "val text 2"
                    }
                ]
            }
        ]
    },
    {
        "id": 4,
        "name": "Rule #4",
        "status": "ENABLED",
        "description": "Rule #4 Description",
        "validateClauses": [
            {
                "id": 4,
                "attributeId": 1,
                "attributeName": "string attribute",
                "attributeType": "string",
                "operator": "eq",
                "condition": [
                    {
                        "type": "string",
                        "value": "val string 1"
                    },
                    {
                        "type": "string",
                        "value": "val string 2"
                    }
                ]
            }
        ],
        "whenClauses": [
            {
                "id": 4,
                "attributeId": 2,
                "attributeName": "text attribute",
                "attributeType": "text",
                "operator": "not eq",
                "condition": [
                    {
                        "type": "text",
                        "value": "val text 1"
                    },
                    {
                        "type": "text",
                        "value": "val text 2"
                    }
                ]
            }
        ]
    },
    {
        "id": 5,
        "name": "Rule #5",
        "status": "ENABLED",
        "description": "Rule #5 Description",
        "validateClauses": [
            {
                "id": 5,
                "attributeId": 1,
                "attributeName": "string attribute",
                "attributeType": "string",
                "operator": "eq",
                "condition": [
                    {
                        "type": "string",
                        "value": "val string 1"
                    },
                    {
                        "type": "string",
                        "value": "val string 2"
                    }
                ]
            }
        ],
        "whenClauses": [
            {
                "id": 5,
                "attributeId": 2,
                "attributeName": "text attribute",
                "attributeType": "text",
                "operator": "not eq",
                "condition": [
                    {
                        "type": "text",
                        "value": "val text 1"
                    },
                    {
                        "type": "text",
                        "value": "val text 2"
                    }
                ]
            }
        ]
    },
    {
        "id": 6,
        "name": "Rule #6",
        "status": "ENABLED",
        "description": "Rule #6 Description",
        "validateClauses": [
            {
                "id": 6,
                "attributeId": 1,
                "attributeName": "string attribute",
                "attributeType": "string",
                "operator": "eq",
                "condition": [
                    {
                        "type": "string",
                        "value": "val string 1"
                    },
                    {
                        "type": "string",
                        "value": "val string 2"
                    }
                ]
            }
        ],
        "whenClauses": [
            {
                "id": 6,
                "attributeId": 2,
                "attributeName": "text attribute",
                "attributeType": "text",
                "operator": "not eq",
                "condition": [
                    {
                        "type": "text",
                        "value": "val text 1"
                    },
                    {
                        "type": "text",
                        "value": "val text 2"
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



