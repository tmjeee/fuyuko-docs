# POST-add-category

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/add-category" %}
{% api-method-summary %}
Add category
{% endapi-method-summary %}

{% api-method-description %}
Add a new category
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

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=true %}
Name
{% endapi-method-parameter %}

{% api-method-parameter name="description" type="string" required=true %}
Description
{% endapi-method-parameter %}

{% api-method-parameter name="parentId" type="number" required=false %}
parent category id \(missing indicate no parent\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "category some category name xxxtest added"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



