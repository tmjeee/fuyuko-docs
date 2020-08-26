---
description: Add item image
---

# POST-add-item-image

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/item/:itemId/image" %}
{% api-method-summary %}
Add item image
{% endapi-method-summary %}

{% api-method-description %}
Add an image to an item.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="itemId" type="number" required=true %}
Item Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication tokens.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-form-data-parameters %}
{% api-method-parameter name="upload1" type="object" required=true %}
Image File
{% endapi-method-parameter %}
{% endapi-method-form-data-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
`upload1` request parameter is expected to be a file. This request require `multipart/form-data` encoding type
{% endhint %}



