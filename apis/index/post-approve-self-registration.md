---
description: Approve self-registration applicants
---

# POST-approve-self-registration

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/self-register/approve/:selfRegistrationId" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
Approve a self registration entry by id.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="selfRegistrationId" type="string" required=true %}
Self-registration application id.
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
  "status": "SUCCESS",
  "message": "....",
  "payload": {
    "email": "self1@gmail.com",
    "message": "Self registration approval for self1 (self1@gmail.com) success",
    "registrationId": 1,
    "status": "SUCCESS",
    "username": "self1"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



