---
description: Create user's dashboard widget data
---

# POST-user-dashboard-widget-data

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/user/:userId/dashboard-widget-instance-data" %}
{% api-method-summary %}
Create user dashboard widget data
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userId" type="number" required=true %}
User ID.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="data" type="string" required=true %}
Widget data
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{ 
    true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
`data` is the JSON format containing

* instanceId
* typeId
* data as string based key value pairs
{% endhint %}

```text
{
   "instanceId": "...",
   "typeId": "...",
   "data": {
      "widget-data-key1": "widget-data-key-value1",
      "widget-data-key2": "widget-data-key-value2"
   }
}
```

