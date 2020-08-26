# GET-Category-Simple-Items-In-Category

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/category/:categoryId/category-simple-items-in-category" %}
{% api-method-summary %}
Get Items In Category
{% endapi-method-summary %}

{% api-method-description %}
Get Items in the given `:categoryId`.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
{% endapi-method-parameter %}

{% api-method-parameter name="categoryId" type="number" required=true %}
Category Id
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
    "message": "Items retrieved successfully",
    "payload": [
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
    "limit": 100,
    "offset": 0,
    "total": 2
}
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



