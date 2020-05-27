---
description: Activate invitation received (eg. through email)
---

# POST-activate-invitation

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/activate-invitation/:code" %}
{% api-method-summary %}
Activate invitation received
{% endapi-method-summary %}

{% api-method-description %}
Activate an invitation sent out by code.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="code" type="string" %}
Invitation code
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
Username
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=true %}
Email
{% endapi-method-parameter %}

{% api-method-parameter name="firstName" type="string" required=true %}
First Name
{% endapi-method-parameter %}

{% api-method-parameter name="lastName" type="string" required=true %}
Last Name
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=true %}
Password
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Invitation activated successfully.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
  "payload": {
    "email": "invitation1@gmail.com",
    "registrationId": 1,
    "message": "Successfully activated invitation1 (invitation1@gmail.com)",
    "status": "SUCCESS",
    "username": "invitation1"
  }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=400 %}
{% api-method-response-example-description %}
Any error with the request
{% endapi-method-response-example-description %}

```
{
    "context": "default",
    "errors": [
        {
            "msg": "Code no longer active",
            "location": "api",
            "param": "code",
            "value": "code1xxx"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



