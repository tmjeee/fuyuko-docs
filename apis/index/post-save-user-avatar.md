---
description: Save user's avatar
---

# POST-save-user-avatar

{% hint style="info" %}
`multipart/form-data` content type
{% endhint %}

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/user/:userId/avatar" %}
{% api-method-summary %}
Save user's avatar
{% endapi-method-summary %}

{% api-method-description %}
Save a user's avatar.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="userId" type="string" required=true %}
User Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="globalAvatarName" type="string" required=false %}
Avatar name
{% endapi-method-parameter %}

{% api-method-parameter name="customAvatarFile" type="object" required=false %}
Avatar file 
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
    "message": "UserId 1, Avatar updated",
    "payload": {
      "userAvatarId": 1
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Either of the following body parameter \(`multipart/form-data`\) must be provided

* `globalAvatarName`
* `customAvatarFile`
{% endhint %}

