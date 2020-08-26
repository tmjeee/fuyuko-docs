# GET-all-favourite-items

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/user/:userId/favourite-items" %}
{% api-method-summary %}
Get all favourite items
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="string" required=true %}
View Id
{% endapi-method-parameter %}

{% api-method-parameter name="userId" type="string" required=true %}
User Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="number" %}
Pagination limit.
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="number" %}
Pagination offset \(zero based\).
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
    "message": "Favourite item retrieved",
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
                    "primary": 0
                },
                {
                    "id": 3,
                    "name": "0003.jpg",
                    "size": 83256,
                    "primary": 0
                }
            ],
            "description": "Item-1 Description",
            "name": "Item-1",
            "creationDate": "2020-06-14T04:07:24.000Z",
            "lastUpdate": "2020-06-14T04:07:24.000Z",
            "children": []
        },
        {
            "id": 5,
            "parentId": null,
            "images": [
                {
                    "id": 13,
                    "name": "0013.jpg",
                    "size": 392173,
                    "primary": 1
                },
                {
                    "id": 14,
                    "name": "0014.jpg",
                    "size": 35669,
                    "primary": 0
                },
                {
                    "id": 15,
                    "name": "0015.jpg",
                    "size": 47898,
                    "primary": 0
                }
            ],
            "description": "Item-3 Description",
            "name": "Item-3",
            "creationDate": "2020-06-14T04:07:24.000Z",
            "lastUpdate": "2020-06-14T04:07:24.000Z",
            "children": []
        },
        {
            "id": 6,
            "parentId": null,
            "images": [
                {
                    "id": 16,
                    "name": "0016.jpg",
                    "size": 177509,
                    "primary": 1
                },
                {
                    "id": 17,
                    "name": "0017.jpg",
                    "size": 281236,
                    "primary": 0
                },
                {
                    "id": 18,
                    "name": "0018.jpg",
                    "size": 95705,
                    "primary": 0
                }
            ],
            "description": "Item-4 Description",
            "name": "Item-4",
            "creationDate": "2020-06-14T04:07:24.000Z",
            "lastUpdate": "2020-06-14T04:07:24.000Z",
            "children": []
        },
        {
            "id": 7,
            "parentId": null,
            "images": [
                {
                    "id": 19,
                    "name": "0019.jpg",
                    "size": 10438,
                    "primary": 1
                },
                {
                    "id": 20,
                    "name": "0020.jpg",
                    "size": 17796,
                    "primary": 0
                },
                {
                    "id": 21,
                    "name": "0021.jpg",
                    "size": 22667,
                    "primary": 0
                }
            ],
            "description": "Item-5 Description",
            "name": "Item-5",
            "creationDate": "2020-06-14T04:07:24.000Z",
            "lastUpdate": "2020-06-14T04:07:24.000Z",
            "children": []
        },
        {
            "id": 8,
            "parentId": null,
            "images": [
                {
                    "id": 22,
                    "name": "0022.jpg",
                    "size": 257902,
                    "primary": 1
                },
                {
                    "id": 23,
                    "name": "0023.jpg",
                    "size": 37701,
                    "primary": 0
                },
                {
                    "id": 24,
                    "name": "0024.jpg",
                    "size": 81916,
                    "primary": 0
                }
            ],
            "description": "Item-6 Description",
            "name": "Item-6",
            "creationDate": "2020-06-14T04:07:24.000Z",
            "lastUpdate": "2020-06-14T04:07:24.000Z",
            "children": []
        }
    ],
    "total": 5,
    "limit": 5,
    "offset": 0
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



