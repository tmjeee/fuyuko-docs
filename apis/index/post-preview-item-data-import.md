---
description: Item data import preview
---

# POST-preview-item-data-import

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/import/items/preview" %}
{% api-method-summary %}
Preview Item Data import
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="itemDataDsvFile" type="object" required=false %}

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
    "type": "ITEM",
    "dataImportId": 5,
    "attributes": [],
    "items": [
        {
            "id": -1,
            "name": "item 1",
            "description": "item 1 description",
            "images": [],
            "parentId": null,
            "children": [
                {
                    "id": -2,
                    "name": "item 1_1",
                    "description": "item 1_1 description",
                    "images": [],
                    "parentId": -1,
                    "children": [
                        {
                            "id": -3,
                            "name": "item 1_1_1",
                            "description": "item 1_1_1 description",
                            "images": [],
                            "parentId": -2,
                            "children": [
                                {
                                    "id": -4,
                                    "name": "item 1_1_1_1",
                                    "description": "item 1_1_1_1 description",
                                    "images": [],
                                    "parentId": -3,
                                    "children": []
                                }
                            ]
                        }
                    ]
                }
            ]
        },
        {
            "id": -5,
            "name": "item 2",
            "description": "item 2 description",
            "images": [],
            "parentId": null,
            "children": []
        },
        {
            "id": -6,
            "name": "item 3",
            "description": "item 3 description",
            "images": [],
            "parentId": null,
            "children": []
        }
    ],
    "messages": {
        "errors": [
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att01 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att02 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att03 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with id 17 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att05 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att06 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att07 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att08 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att09 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att10 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att11 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att12 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 2: Attribute with name att13 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att01 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att02 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att03 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with id 17 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att05 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att06 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att07 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att08 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att09 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att10 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att11 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att12 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 3: Attribute with name att13 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att01 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att02 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att03 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with id 17 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att05 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att06 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att07 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att08 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att09 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att10 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att11 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att12 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 4: Attribute with name att13 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att01 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att02 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att03 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with id 17 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att05 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att06 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att07 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att08 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att09 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att10 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att11 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att12 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 5: Attribute with name att13 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att01 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att02 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att03 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with id 17 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att05 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att06 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att07 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att08 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att09 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att10 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att11 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att12 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 6: Attribute with name att13 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att01 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att02 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att03 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with id 17 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att05 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att06 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att07 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att08 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att09 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att10 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att11 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att12 not found in view 3"
            },
            {
                "title": "Attribute not found",
                "messsage": "Line 7: Attribute with name att13 not found in view 3"
            }
        ],
        "infos": [],
        "warnings": []
    }
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
* Needs to be `mutiplart/form-data` content-type
* Request body`itemDataCsvFile` attribute is a `multipart/form-dataFile` object
{% endhint %}





