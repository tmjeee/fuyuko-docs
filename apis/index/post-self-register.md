---
description: Self registration
---

# POST-self-register

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/self-register" %}
{% api-method-summary %}
Self Registration
{% endapi-method-summary %}

{% api-method-description %}
Self register with the system.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
  "payload": {
    "registrationId": 100,
    "email": "ccccctest1@gmail.com",
    "username": "ccccctest1",
    "status": "SUCCESS",
    "message": "User ccccctest1 (ccccctest1@gmail.com) registered"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



