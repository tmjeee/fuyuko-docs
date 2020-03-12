---
description: Save user
---

# POST-save-user

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/user" %}
{% api-method-summary %}
Save user
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="userId" type="string" required=false %}
User Id
{% endapi-method-parameter %}

{% api-method-parameter name="firstName" type="string" required=false %}
First Name
{% endapi-method-parameter %}

{% api-method-parameter name="lastName" type="string" required=false %}
Last Name
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
Email
{% endapi-method-parameter %}

{% api-method-parameter name="theme" type="string" required=false %}
Theme
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=false %}
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
{    "name": "Cake's name",    "recipe": "Cake's recipe name",    "cake": "Binary cake"}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "Ain't no cake like that."}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Either of the following body parameter must be provided

* `firstName`
* `lastName`
* `email`
* `theme`
* `password`
{% endhint %}

