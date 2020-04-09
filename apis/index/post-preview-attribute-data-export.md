---
description: Preview Attribute Data Export
---

# POST-preview-attribute-data-export

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/export/attributes/preview" %}
{% api-method-summary %}
Preview Data Export
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="attributes" type="array" required=false %}
Attributes
{% endapi-method-parameter %}

{% api-method-parameter name="filter" type="array" required=false %}
Filter
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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
  "payload": {
    "type": "ATTRIBUTE",
    "attributes": [
        {
            "id": 14,
            "name": "att01",
            "description": "att 01 description",
            "type": "string"
        },
        {
            "id": 15,
            "name": "att02",
            "description": "att 02 description",
            "type": "text"
        },
        {
            "id": 16,
            "name": "att03",
            "description": "att 03 description",
            "type": "number",
            "format": "0.0"
        },
        {
            "id": 17,
            "name": "att04",
            "description": "att 04 description",
            "type": "date",
            "format": "DD/MM/YYYY"
        },
        {
            "id": 18,
            "name": "att05",
            "description": "att 05 description",
            "type": "currency",
            "showCurrencyCountry": true
        },
        {
            "id": 19,
            "name": "att06",
            "description": "att 06 description",
            "type": "volume",
            "format": "0.0"
        },
        {
            "id": 20,
            "name": "att07",
            "description": "att 07 description",
            "type": "dimension",
            "format": "0.0"
        },
        {
            "id": 21,
            "name": "att08",
            "description": "att 08 description",
            "type": "area",
            "format": "0.0"
        },
        {
            "id": 22,
            "name": "att09",
            "description": "att 09 description",
            "type": "width",
            "format": "0.0"
        },
        {
            "id": 23,
            "name": "att10",
            "description": "att 10 description",
            "type": "length",
            "format": "0.0"
        },
        {
            "id": 24,
            "name": "att11",
            "description": "att 11 description",
            "type": "height",
            "format": "0.0"
        },
        {
            "id": 25,
            "name": "att12",
            "description": "att 12 description",
            "type": "select",
            "pair1": [
                {
                    "id": 118,
                    "key": "key1",
                    "value": "value1"
                },
                {
                    "id": 119,
                    "key": "key2",
                    "value": "value2"
                },
                {
                    "id": 120,
                    "key": "key3",
                    "value": "value3"
                }
            ]
        },
        {
            "id": 26,
            "name": "att13",
            "description": "att 13 description",
            "type": "doubleselect",
            "pair1": [
                {
                    "id": 121,
                    "key": "key1",
                    "value": "value1"
                },
                {
                    "id": 122,
                    "key": "key2",
                    "value": "value2"
                },
                {
                    "id": 123,
                    "key": "key3",
                    "value": "value3"
                }
            ],
            "pair2": [
                {
                    "id": 124,
                    "key1": "key1",
                    "key2": "xkey11",
                    "value": "xvalue11"
                },
                {
                    "id": 125,
                    "key1": "key1",
                    "key2": "xkey12",
                    "value": "xvalue12"
                },
                {
                    "id": 126,
                    "key1": "key2",
                    "key2": "xkey21",
                    "value": "xvalue21"
                },
                {
                    "id": 127,
                    "key1": "key2",
                    "key2": "xkey22",
                    "value": "xvalue22"
                },
                {
                    "id": 128,
                    "key1": "key3",
                    "key2": "xkey31",
                    "value": "xvalue31"
                },
                {
                    "id": 129,
                    "key1": "key3",
                    "key2": "xkey32",
                    "value": "xvalue32"
                }
            ]
        }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



