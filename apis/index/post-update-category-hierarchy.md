# POST-update-category-hierarchy

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/v1//view/:viewId/category/:categoryId/parentId/:parentCategoryId/update-hierarchy" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
viewId
{% endapi-method-parameter %}

{% api-method-parameter name="categoryId" type="number" required=true %}
categoryId of category that needs changing
{% endapi-method-parameter %}

{% api-method-parameter name="parentCategoryId" type="string" required=true %}
parentCategoryId \(as number\) or null if no parent category
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication jwt token
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
    "message": "category 10 hierarchy updated"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



