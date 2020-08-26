---
description: Get an item's primary image
---

# GET-item-primary-image

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/item/image/primary/:itemId" %}
{% api-method-summary %}
Get an item's primary image
{% endapi-method-summary %}

{% api-method-description %}
Get Item's primary image
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="itemId" type="number" required=true %}
Item Id.
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

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Return the item's primary image in bytes
{% endhint %}

