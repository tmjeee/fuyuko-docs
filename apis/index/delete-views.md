---
description: Delete views
---

# DELETE-views

{% api-method method="delete" host="https://<host>:<port>/api/v1" path="/views/delete" %}
{% api-method-summary %}
Delete views
{% endapi-method-summary %}

{% api-method-description %}
Delete views by Ids.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="\*.id" type="number" required=true %}
JSON object with a id property \(View's ID\)
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
  "message": "....",
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Request body is a JSON array of objects containing an id property indicating the view's ID.

```text
[ // body
   { id: 1 },
   { id: 2 }
   ...
]
```
{% endhint %}



