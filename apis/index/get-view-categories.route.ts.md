# GET-view-categories.route.ts

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/categories" %}
{% api-method-summary %}
Get view categories
{% endapi-method-summary %}

{% api-method-description %}
Get all categories in a `:viewId`
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
            "children": [
                {
                    "id": 2,
                    "name": "Category-1-1",
                    "description": "Category 1-1 description",
                    "status": "ENABLED",
                    "creationDate": "2020-05-04T14:14:36.000Z",
                    "lastUpdate": "2020-05-04T14:14:36.000Z",
                    "children": [
                        {
                            "id": 3,
                            "name": "Category-1-1-1",
                            "description": "Category 1-1-1 description",
                            "status": "ENABLED",
                            "creationDate": "2020-05-04T14:14:36.000Z",
                            "lastUpdate": "2020-05-04T14:14:36.000Z",
                            "children": []
                        },
                        {
                            "id": 4,
                            "name": "Category-1-1-2",
                            "description": "Category 1-1-2 description",
                            "status": "ENABLED",
                            "creationDate": "2020-05-04T14:14:36.000Z",
                            "lastUpdate": "2020-05-04T14:14:36.000Z",
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
                    "children": [
                        {
                            "id": 6,
                            "name": "Category-1-2-1",
                            "description": "Category 1-2-1 description",
                            "status": "ENABLED",
                            "creationDate": "2020-05-04T14:14:36.000Z",
                            "lastUpdate": "2020-05-04T14:14:36.000Z",
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
            "children": [
                {
                    "id": 8,
                    "name": "Category-2-1",
                    "description": "Category 2-1 description",
                    "status": "ENABLED",
                    "creationDate": "2020-05-04T14:14:36.000Z",
                    "lastUpdate": "2020-05-04T14:14:36.000Z",
                    "children": []
                },
                {
                    "id": 9,
                    "name": "Category-2-2",
                    "description": "Category 2-2 description",
                    "status": "ENABLED",
                    "creationDate": "2020-05-04T14:14:36.000Z",
                    "lastUpdate": "2020-05-04T14:14:36.000Z",
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
            "children": []
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/categories-with-items" %}
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
Action successfully executed.
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/categories-with-items" %}
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
Action successfully executed.
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



