# GET-all-favourite-item-ids

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/user/:userId/favourite-item-ids" %}
{% api-method-summary %}
Get all favourite item ids
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View id
{% endapi-method-parameter %}

{% api-method-parameter name="userId" type="number" required=true %}
User id
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
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "Favourite item ids retrieved",
    "payload": [
        5,
        6,
        1,
        7,
        8
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



