# GET-view-category-items

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/category/:categoryId/items" %}
{% api-method-summary %}
Get view category items
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="categoryId" type="number" required=true %}
Category Id
{% endapi-method-parameter %}

{% api-method-parameter name="viewId" type="number" required=true %}
 View Id.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="number" required=false %}
Limit for pagination
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="number" required=false %}
Offset for pagination
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "success",
    "payload": [
        {
            "1": {
                "attributeId": 1,
                "val": {
                    "type": "string",
                    "value": "some string"
                }
            },
            "2": {
                "attributeId": 2,
                "val": {
                    "type": "text",
                    "value": "some text"
                }
            },
            "id": 1,
            "parentId": null,
            "images": [
                {
                    "id": 1,
                    "name": "0001.jpg",
                    "size": 57466,
                    "primary": 1
                },
                {
                    "id": 2,
                    "name": "0002.jpg",
                    "size": 124300,
                    "primary": 1
                },
                {
                    "id": 3,
                    "name": "0003.jpg",
                    "size": 83256,
                    "primary": 1
                }
            ],
            "description": "Item-1 Description",
            "name": "Item-1",
            "creationDate": "2020-05-04T14:14:36.000Z",
            "lastUpdate": "2020-05-04T14:14:36.000Z",
            "children": [
                {
                    "id": 2,
                    "parentId": 1,
                    "images": [
                        {
                            "id": 4,
                            "name": "0004.jpg",
                            "size": 75170,
                            "primary": 1
                        },
                        {
                            "id": 5,
                            "name": "0005.jpg",
                            "size": 26242,
                            "primary": 1
                        },
                        {
                            "id": 6,
                            "name": "0006.jpg",
                            "size": 38305,
                            "primary": 1
                        }
                    ],
                    "description": "Item-1-1 Description",
                    "name": "Item-1-1",
                    "creationDate": "2020-05-04T14:14:36.000Z",
                    "lastUpdate": "2020-05-04T14:14:36.000Z",
                    "children": []
                },
                {
                    "id": 3,
                    "parentId": 1,
                    "images": [
                        {
                            "id": 7,
                            "name": "0007.jpg",
                            "size": 223083,
                            "primary": 1
                        },
                        {
                            "id": 8,
                            "name": "0008.jpg",
                            "size": 37514,
                            "primary": 1
                        },
                        {
                            "id": 9,
                            "name": "0009.jpg",
                            "size": 85183,
                            "primary": 1
                        }
                    ],
                    "description": "Item-1-2 Description",
                    "name": "Item-1-2",
                    "creationDate": "2020-05-04T14:14:36.000Z",
                    "lastUpdate": "2020-05-04T14:14:36.000Z",
                    "children": []
                }
            ]
        },
        {
            "id": 4,
            "parentId": null,
            "images": [
                {
                    "id": 10,
                    "name": "0010.jpg",
                    "size": 23016,
                    "primary": 1
                },
                {
                    "id": 11,
                    "name": "0011.jpg",
                    "size": 115737,
                    "primary": 1
                },
                {
                    "id": 12,
                    "name": "0012.jpg",
                    "size": 15793,
                    "primary": 1
                }
            ],
            "description": "Item-2 Description",
            "name": "Item-2",
            "creationDate": "2020-05-04T14:14:36.000Z",
            "lastUpdate": "2020-05-04T14:14:36.000Z",
            "children": []
        }
    ],
    "limit": 2,
    "offset": 0,
    "total": 2
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



