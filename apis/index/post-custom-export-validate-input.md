---
description: Validate custom export's inputs
---

# POST-custom-export-validate-input

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/custom-export/:customExportId/validate-input" %}
{% api-method-summary %}
Validate Custom Export's Inputs
{% endapi-method-summary %}

{% api-method-description %}
Validate input\(s\) of a custom export.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View ID
{% endapi-method-parameter %}

{% api-method-parameter name="customExportId" type="number" required=true %}
Custom Export Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="values" type="array" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="values.\*.type" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="values.\*.name" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="values.\*.value" type="string" required=false %}

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
  "message": "...",
  "payload":{
    "valid": true,
    "messages": [
        {
            "status": "INFO",
            "title": "sample info title",
            "message": "sample info message"
        }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
`values` is expected to be a `JSON Array` with object of `type`, `name` and `value` properties
{% endhint %}



