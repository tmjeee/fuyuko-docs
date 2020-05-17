# GET-Category-Simple-Items-Not-In-Category

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/category/:categoryId/category-simple-items-not-in-category" %}
{% api-method-summary %}
Get Items Not In Category
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

{% api-method-parameter name="categoryId" type="string" required=true %}
Category Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="Authentication" type="string" required=true %}
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
    "message": "Items retrieved successfully",
    "payload": [
        {
            "id": 5,
            "name": "Item-3",
            "description": "Item-3 Description"
        },
        {
            "id": 6,
            "name": "Item-4",
            "description": "Item-4 Description"
        },
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
    "limit": 100,
    "offset": 0,
    "total": 5
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



