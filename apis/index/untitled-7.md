# POST-add-item-to-category

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/category/:categoryId/item/:itemId" %}
{% api-method-summary %}
Add item to category
{% endapi-method-summary %}

{% api-method-description %}
Add Item to a category
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

{% api-method-parameter name="itemId" type="number" required=true %}
Item Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication Token.
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
    "message": "item id 2 added to category 21 in view 2"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



