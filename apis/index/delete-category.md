# DELETE-category

{% api-method method="delete" host="https://<host>:<port>/api/v1" path="/view/:viewId/category/:categoryId" %}
{% api-method-summary %}
Delete category
{% endapi-method-summary %}

{% api-method-description %}
Delete a category
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="string" required=true %}
View ID
{% endapi-method-parameter %}

{% api-method-parameter name="categoryId" type="string" required=true %}
Category ID
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
Successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "Category 21 in view 2 deleted"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



