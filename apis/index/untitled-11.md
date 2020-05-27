# GET-view-categories-with-items

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/categories-with-items" %}
{% api-method-summary %}
Get view categories with items
{% endapi-method-summary %}

{% api-method-description %}
Get categories in `:viewId` together with all items in it.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
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
Action successfully executed.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "success",
    "payload": [
        {
            "id": 1,
            "name": "Category-1",
            "description": "Category 1 description",
            "status": "ENABLED",
            "creationDate": "2020-05-04T14:14:36.000Z",
            "lastUpdate": "2020-05-04T14:14:36.000Z",
            "items": [
                {
                    "id": 1,
                    "name": "Item-1",
                    "description": "Item-1 Description"
                },
                {
                    "id": 4,
                    "name": "Item-2",
                    "description": "Item-2 Description"
                }
            ],
            "children": [
                {
                    "id": 2,
                    "name": "Category-1-1",
                    "description": "Category 1-1 description",
                    "status": "ENABLED",
                    "creationDate": "2020-05-04T14:14:36.000Z",
                    "lastUpdate": "2020-05-04T14:14:36.000Z",
                    "items": [
                        {
                            "id": 5,
                            "name": "Item-3",
                            "description": "Item-3 Description"
                        },
                        {
                            "id": 6,
                            "name": "Item-4",
                            "description": "Item-4 Description"
                        }
                    ],
                    "children": [
                        {
                            "id": 3,
                            "name": "Category-1-1-1",
                            "description": "Category 1-1-1 description",
                            "status": "ENABLED",
                            "creationDate": "2020-05-04T14:14:36.000Z",
                            "lastUpdate": "2020-05-04T14:14:36.000Z",
                            "items": [
                                {
                                    "id": 7,
                                    "name": "Item-5",
                                    "description": "Item-5 Description"
                                },
                                {
                                    "id": 8,
                                    "name": "Item-6",
                                    "description": "Item-6 Description"
                                },
                                {
                                    "id": 9,
                                    "name": "Item-7",
                                    "description": "Item-7 Description"
                                }
                            ],
                            "children": []
                        },
                        {
                            "id": 4,
                            "name": "Category-1-1-2",
                            "description": "Category 1-1-2 description",
                            "status": "ENABLED",
                            "creationDate": "2020-05-04T14:14:36.000Z",
                            "lastUpdate": "2020-05-04T14:14:36.000Z",
                            "items": [],
                            "children": []
                        }
                    ]
                },
                {
                    "id": 5,
                    "name": "Category-1-2",
                    "description": "Category 1-2 description",
                    "status": "ENABLED",
                    "creationDate": "2020-05-04T14:14:36.000Z",
                    "lastUpdate": "2020-05-04T14:14:36.000Z",
                    "items": [],
                    "children": [
                        {
                            "id": 6,
                            "name": "Category-1-2-1",
                            "description": "Category 1-2-1 description",
                            "status": "ENABLED",
                            "creationDate": "2020-05-04T14:14:36.000Z",
                            "lastUpdate": "2020-05-04T14:14:36.000Z",
                            "items": [],
                            "children": []
                        }
                    ]
                }
            ]
        },
        {
            "id": 7,
            "name": "Category-2",
            "description": "Category 2 description",
            "status": "ENABLED",
            "creationDate": "2020-05-04T14:14:36.000Z",
            "lastUpdate": "2020-05-04T14:14:36.000Z",
            "items": [],
            "children": [
                {
                    "id": 8,
                    "name": "Category-2-1",
                    "description": "Category 2-1 description",
                    "status": "ENABLED",
                    "creationDate": "2020-05-04T14:14:36.000Z",
                    "lastUpdate": "2020-05-04T14:14:36.000Z",
                    "items": [],
                    "children": []
                },
                {
                    "id": 9,
                    "name": "Category-2-2",
                    "description": "Category 2-2 description",
                    "status": "ENABLED",
                    "creationDate": "2020-05-04T14:14:36.000Z",
                    "lastUpdate": "2020-05-04T14:14:36.000Z",
                    "items": [],
                    "children": []
                }
            ]
        },
        {
            "id": 10,
            "name": "Category-3",
            "description": "Category-3",
            "status": "ENABLED",
            "creationDate": "2020-05-04T14:14:37.000Z",
            "lastUpdate": "2020-05-04T14:14:37.000Z",
            "items": [],
            "children": []
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/category/:categoryId/items" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Actions successfully executed.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/category/:categoryId/items" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Actions successfully executed.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/forgot-password/code/:code/reset" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Action succussfully executed.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



