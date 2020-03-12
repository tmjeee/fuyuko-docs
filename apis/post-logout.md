---
description: Logout from the application
---

# Post-logout

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/logout" %}
{% api-method-summary %}
Logout
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "ok": true,
    "message": "Logged out, have a nice day"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



