---
description: Get user dashboard
---

# GET-user-dashboard.route.ts

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/user/:userId/dashboard" %}
{% api-method-summary %}
Get user dashboard
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userId" type="string" required=true %}
User Id.
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
    "data": "\"{\\\"strategyId\\\":\\\"2x\\\",\\\"instances\\\":[{\\\"instanceId\\\":\\\"9349cd40-6e83-11ea-ac04-5ddd8bc50828\\\",\\\"typeId\\\":\\\"sample-1-widget\\\"},{\\\"instanceId\\\":\\\"94325880-6e83-11ea-ac04-5ddd8bc50828\\\",\\\"typeId\\\":\\\"sample-2-widget\\\"}],\\\"special\\\":[[{\\\"instanceId\\\":\\\"9349cd40-6e83-11ea-ac04-5ddd8bc50828\\\",\\\"typeId\\\":\\\"sample-1-widget\\\"}],[{\\\"instanceId\\\":\\\"94325880-6e83-11ea-ac04-5ddd8bc50828\\\",\\\"typeId\\\":\\\"sample-2-widget\\\"}]]}\""
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



