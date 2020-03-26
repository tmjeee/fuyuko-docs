---
description: Get user dashboard data
---

# GET-user-dashboard-widget-data

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/user/:userId/dashboard-widget-instance/:dashboardWidgetInstanceId" %}
{% api-method-summary %}
User dashboard widget data
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userId" type="number" required=true %}
User Id
{% endapi-method-parameter %}

{% api-method-parameter name="dashboardWidgetInstanceId" type="string" required=true %}
Dashboard widget instance id \(string\)
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
    "key1": "value1",
    "key2": "value2"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



