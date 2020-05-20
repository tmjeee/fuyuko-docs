# POST-check-forgot-password-code

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/forgot-password/code/:code/validity" %}
{% api-method-summary %}
Check Validity of Forgot Password code
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="code" type="string" required=true %}
Forgot Password Code
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
    "message": "Validity retrieved",
    "payload": true
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



