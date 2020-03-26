---
description: Delete item image by id
---

# DELETE-item-image-by-id

{% api-method method="delete" host="https://<host>:<port>/api/v1" path="/item/:itemId/image/:itemImageId" %}
{% api-method-summary %}
Delete item image by id
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="itemId" type="number" required=true %}
Item Id
{% endapi-method-parameter %}

{% api-method-parameter name="itemImageId" type="number" required=true %}
Item Image Id
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
true
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



