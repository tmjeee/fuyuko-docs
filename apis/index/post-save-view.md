---
description: Save view
---

# POST-save-view

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/views/update" %}
{% api-method-summary %}
Save view
{% endapi-method-summary %}

{% api-method-description %}
Save a view.  
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="\*.name" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="\*.description" type="string" required=false %}

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
    "message": "views updated"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Request body parameter is a JSON array
{% endhint %}

