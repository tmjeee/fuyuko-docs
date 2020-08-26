---
description: Get help content
---

# GET-help

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/help/:helpPostfix" %}
{% api-method-summary %}
Get help content
{% endapi-method-summary %}

{% api-method-description %}
Get help based on given `:helpPostfix`.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="helpPostfix" type="string" required=true %}
String to help indicate which help content to retrieve
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
Help content successfully retrieved.
{% endapi-method-response-example-description %}

```
Dashboard help placeholder
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
The response content will be the html of the help content. 
{% endhint %}



