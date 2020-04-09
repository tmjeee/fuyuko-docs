---
description: Change custom rule status
---

# POST-change-custom-rule-status

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/custom-rules/:customRuleId/status/:status" %}
{% api-method-summary %}
Change custom rule status
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View ID
{% endapi-method-parameter %}

{% api-method-parameter name="customRuleId" type="number" required=true %}
Custom Rule ID
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=true %}
Status
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token .
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
  "message": "...."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



