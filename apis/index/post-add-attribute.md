---
description: Add attribute
---

# POST-add-attribute

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/attributes/add" %}
{% api-method-summary %}
Add attribute
{% endapi-method-summary %}

{% api-method-description %}
Add an item attribute.
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
{% api-method-parameter name="attributes" type="array" required=false %}
`attributes` JSON array
{% endapi-method-parameter %}

{% api-method-parameter name="attributes.\*.type" type="string" required=false %}
Attribute type
{% endapi-method-parameter %}

{% api-method-parameter name="attributes.\*.name" type="string" required=false %}
Attribute name
{% endapi-method-parameter %}

{% api-method-parameter name="attributes.\*.description" type="string" required=false %}
Attribute description
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
    "message": "Attributes added"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
`attributes` request body parameter is expected to be a JSON Array
{% endhint %}



