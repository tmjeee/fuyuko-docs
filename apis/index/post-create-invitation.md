---
description: Create an invitation (include sending out email) for using the application
---

# POST-create-invitation

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/create-invitation" %}
{% api-method-summary %}
Create invitation
{% endapi-method-summary %}

{% api-method-description %}
Create and sent out an invitation to join the system.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=true %}
Email to sent invitation to.
{% endapi-method-parameter %}

{% api-method-parameter name="groupIds.\*" type="number" required=true %}
Group Ids this user will be in upon activation
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
    "message": "Invitation Created"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
`groupIds` property is expected to be a JSON array. Example of the body would look as follows:

```text
{
  email: "....",
  groupIds: [ 1,2,3 ]
}
```
{% endhint %}

