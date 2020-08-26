---
description: Create user notification
---

# POST-user-notification

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/user/:userId/notification" %}
{% api-method-summary %}
Create user notification
{% endapi-method-summary %}

{% api-method-description %}
Publish a user notification.
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

{% api-method-body-parameters %}
{% api-method-parameter name="notification" type="object" required=false %}
Notification JSON object
{% endapi-method-parameter %}

{% api-method-parameter name="notification.status" type="string" required=true %}
Status
{% endapi-method-parameter %}

{% api-method-parameter name="notification.title" type="string" required=true %}
TItle
{% endapi-method-parameter %}

{% api-method-parameter name="notification.description" type="string" required=true %}
Description
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
  "message": "....",
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



