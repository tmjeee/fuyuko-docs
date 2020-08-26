---
description: Get the global avatar by name
---

# GET-global-avatar

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/global/avatar/:avatarName" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
Get a global avatar by it's name.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="avatarName" type="string" required=true %}
Global Avatar's Name
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Global avatar image in bytes successfully returned
{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



