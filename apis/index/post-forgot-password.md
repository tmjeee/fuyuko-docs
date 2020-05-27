# POST-forgot-password

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/forgot-password" %}
{% api-method-summary %}
Send Forgotten Password
{% endapi-method-summary %}

{% api-method-description %}
Trigger a reset password action.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="username" type="string" required=false %}
Username
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
Email
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
    "message": "Forgot email password sent"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Either `username` or `email` body parameter needs to exists else an error will be returned.
{% endhint %}



