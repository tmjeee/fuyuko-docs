# GET-all-custom-bulk-edit

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/custom-bulk-edits" %}
{% api-method-summary %}
Get all custom bulk edit
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
Custom bulk edit successfully retrieved
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "Custom Bulk Edit retrieval success",
    "payload": [
        {
            "id": 1,
            "name": "0.0.1-sample-custom-bulk-edit-1.js",
            "description": "0.0.1-sample-custom-bulk-edit-1 description",
            "creationDate": "2020-06-11T05:05:36.000Z",
            "lastUpdate": "2020-06-11T05:05:36.000Z",
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
            "name": "0.0.2-sample-custom-bulk-edit-2.js",
            "description": "0.0.2-sample-custom-bulk-edit-2 description",
            "creationDate": "2020-06-11T05:05:36.000Z",
            "lastUpdate": "2020-06-11T05:05:36.000Z",
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
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



