---
description: Attribute data import preview
---

# POST-preview-attribute-data-import

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/import/attributes/preview" %}
{% api-method-summary %}
Preview attribute data import
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View ID
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="attributeDataCsvFile" type="object" required=false %}

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
    "dataImportId": 3,
    "messages": {
        "errors": [],
        "infos": [],
        "warnings": []
    },
    "attributes": [
        {
            "id": -1,
            "name": "att01",
            "description": "att 01 description",
            "format": "",
            "showCurrencyCountry": false,
            "type": "string",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att02",
            "description": "att 02 description",
            "format": "",
            "showCurrencyCountry": false,
            "type": "text",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att03",
            "description": "att 03 description",
            "format": "0.0",
            "showCurrencyCountry": false,
            "type": "number",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att04",
            "description": "att 04 description",
            "format": "DD/MM/YYYY",
            "showCurrencyCountry": false,
            "type": "date",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att05",
            "description": "att 05 description",
            "format": "",
            "showCurrencyCountry": true,
            "type": "currency",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att06",
            "description": "att 06 description",
            "format": "0.0",
            "showCurrencyCountry": false,
            "type": "volume",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att07",
            "description": "att 07 description",
            "format": "0.0",
            "showCurrencyCountry": false,
            "type": "dimension",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att08",
            "description": "att 08 description",
            "format": "0.0",
            "showCurrencyCountry": false,
            "type": "area",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att09",
            "description": "att 09 description",
            "format": "0.0",
            "showCurrencyCountry": false,
            "type": "width",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att10",
            "description": "att 10 description",
            "format": "0.0",
            "showCurrencyCountry": false,
            "type": "length",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att11",
            "description": "att 11 description",
            "format": "0.0",
            "showCurrencyCountry": false,
            "type": "height",
            "pair1": [],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att12",
            "description": "att 12 description",
            "format": "",
            "showCurrencyCountry": false,
            "type": "select",
            "pair1": [
                {
                    "id": -1,
                    "key": "key1",
                    "value": "value1"
                },
                {
                    "id": -1,
                    "key": "key2",
                    "value": "value2"
                },
                {
                    "id": -1,
                    "key": "key3",
                    "value": "value3"
                }
            ],
            "pair2": []
        },
        {
            "id": -1,
            "name": "att13",
            "description": "att 13 description",
            "format": "",
            "showCurrencyCountry": false,
            "type": "doubleselect",
            "pair1": [
                {
                    "id": -1,
                    "key": "key1",
                    "value": "value1"
                },
                {
                    "id": -1,
                    "key": "key2",
                    "value": "value2"
                },
                {
                    "id": -1,
                    "key": "key3",
                    "value": "value3"
                }
            ],
            "pair2": [
                {
                    "id": -1,
                    "key1": "key1",
                    "key2": "xkey11",
                    "value": "xvalue11"
                },
                {
                    "id": -1,
                    "key1": "key1",
                    "key2": "xkey12",
                    "value": "xvalue12"
                },
                {
                    "id": -1,
                    "key1": "key2",
                    "key2": "xkey21",
                    "value": "xvalue21"
                },
                {
                    "id": -1,
                    "key1": "key2",
                    "key2": "xkey22",
                    "value": "xvalue22"
                },
                {
                    "id": -1,
                    "key1": "key3",
                    "key2": "xkey31",
                    "value": "xvalue31"
                },
                {
                    "id": -1,
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

{% hint style="info" %}
* Needs to be `mutiplart/form-data` content-type
* Request body `attributeDataCsvFile` attribute is a `multipart/form-dataFile` object
{% endhint %}

