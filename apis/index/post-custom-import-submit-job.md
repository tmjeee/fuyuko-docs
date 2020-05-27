---
description: Submit a custom import job
---

# POST-custom-import-submit-job

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/custom-import/:customImportId/submit-job" %}
{% api-method-summary %}
Submit a custom import job
{% endapi-method-summary %}

{% api-method-description %}
Submit a custom import job to be scheduled for execution.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="string" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="values" type="array" required=false %}
Inputs
{% endapi-method-parameter %}

{% api-method-parameter name="values.\*.type" type="string" required=false %}
Individual input type
{% endapi-method-parameter %}

{% api-method-parameter name="values.\*.name" type="string" required=false %}
Individual input name
{% endapi-method-parameter %}

{% api-method-parameter name="values.\*.value" type="string" required=false %}
Individual input value
{% endapi-method-parameter %}

{% api-method-parameter name="preview" type="object" required=false %}
The preview object from preview request step
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
  "message": "...",
  "payload": {
    "valid": true,
    "messages": [
        {
            "status": "INFO",
            "title": "Success",
            "message": "Custom import job 0.0.1-sample-custom-import-1.js-42a5f788-88d5-4c94-ad11-93334fd5947d submitted"
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
* `value` is expected to be a `JSON Array` containing object with `type`, `name` and `value` properties
* `preview` is a `JSON Object` obtained during preview request
{% endhint %}



