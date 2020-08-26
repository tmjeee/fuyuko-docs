---
description: Update rule status
---

# POST-update-rule-status

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/rule/:ruleId/status/:status" %}
{% api-method-summary %}
Update rule status
{% endapi-method-summary %}

{% api-method-description %}
Update a rule's status in a view.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=false %}
View Id
{% endapi-method-parameter %}

{% api-method-parameter name="ruleId" type="number" required=false %}
Rule Id
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" %}
Status Code.
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
Successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "Status updated"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



