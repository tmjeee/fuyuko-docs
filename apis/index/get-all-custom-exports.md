---
description: Get all custom exports
---

# GET-all-custom-exports

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/custom-exports" %}
{% api-method-summary %}
Get all custom exports
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
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
  "payload":[
    {
        "id": 1,
        "name": "0.0.1-sample-custom-export-1.js",
        "description": "0.0.1-sample-custom-import-1 description",
        "creationDate": "2020-04-07T02:57:10.000Z",
        "lastUpdate": "2020-04-07T02:57:10.000Z",
        "inputs": [
            {
                "type": "string",
                "name": "string input",
                "description": "string input description"
            },
            {
                "type": "number",
                "name": "number input",
                "description": "number input description"
            },
            {
                "type": "date",
                "name": "date input",
                "description": "date input description"
            },
            {
                "type": "checkbox",
                "name": "checkbox input",
                "description": "checkbox input description"
            },
            {
                "type": "select",
                "name": "select input",
                "description": "select input description",
                "options": [
                    {
                        "key": "key1",
                        "value": "value1"
                    },
                    {
                        "key": "key2",
                        "value": "value2"
                    },
                    {
                        "key": "key3",
                        "value": "value3"
                    },
                    {
                        "key": "key4",
                        "value": "value4"
                    }
                ]
            },
            {
                "type": "file",
                "name": "file input",
                "description": "file input description"
            }
        ]
    },
    {
        "id": 2,
        "name": "0.0.2-sample-custom-export-2.js",
        "description": "0.0.1-sample-custom-import-1 description",
        "creationDate": "2020-04-07T02:57:10.000Z",
        "lastUpdate": "2020-04-07T02:57:10.000Z",
        "inputs": [
            {
                "type": "string",
                "name": "string input",
                "description": "string xxx input description"
            },
            {
                "type": "number",
                "name": "number input",
                "description": "number xxx input description"
            },
            {
                "type": "date",
                "name": "date input",
                "description": "date xxx input description"
            },
            {
                "type": "checkbox",
                "name": "checkbox input",
                "description": "checkbox xxx input description"
            },
            {
                "type": "select",
                "name": "select input",
                "description": "select xxx input description",
                "options": [
                    {
                        "key": "key1",
                        "value": "value1"
                    },
                    {
                        "key": "key2",
                        "value": "value2"
                    },
                    {
                        "key": "key3",
                        "value": "value3"
                    },
                    {
                        "key": "key4",
                        "value": "value4"
                    }
                ]
            },
            {
                "type": "file",
                "name": "file input",
                "description": "file xxx input description"
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



