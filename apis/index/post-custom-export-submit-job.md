---
description: Submit custom export job
---

# POST-custom-export-submit-job

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/custom-export/:customExportId/submit-job" %}
{% api-method-summary %}
Submit custom export job
{% endapi-method-summary %}

{% api-method-description %}
Submit a custom export job for scheduled exection.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
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
{% api-method-parameter name="views" type="array" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="views.\*.name" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="views.\*.type" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="views.\*.value" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="preview" type="object" required=false %}

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
            "title": "Success",
            "message": "Custom export job 0.0.1-sample-custom-export-1.js-f7eaf241-41a0-4cf2-ba9f-5a30f76bfcc3 submitted"
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
* `views` is expected to be a `JSON Array` containing object with `name`, `type` and `value` properties
* `preview` is expected to be a `JSON Object` obtained from preview request
{% endhint %}

