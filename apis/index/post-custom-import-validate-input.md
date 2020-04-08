---
description: Validate inputs of custom import
---

# POST-custom-import-validate-input

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/custom-import/:customImportId/validate-input" %}
{% api-method-summary %}
Validate custom import's inputs
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
{% endapi-method-parameter %}

{% api-method-parameter name="customImportId" type="number" required=true %}
Custom Import Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="values" type="string" required=true %}

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
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "valid": true,
    "messages": [
        {
            "status": "INFO",
            "title": "sample info title",
            "message": "sample info message"
        }
    ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



