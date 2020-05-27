---
description: Get user notifications
---

# GET-user-notification

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/user/:userId/notifications" %}
{% api-method-summary %}
User notifications
{% endapi-method-summary %}

{% api-method-description %}
Get a user's notifications.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userId" type="number" required=true %}
User ID
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
{
  "status": "SUCCESS",
  "message": "....",
  "payload": [
    {
        "id": 1,
        "isNew": 1,
        "status": "INFO",
        "title": "Notification 1",
        "message": "Simple notification one"
    }
  ]
}Ge
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



