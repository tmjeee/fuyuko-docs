---
description: Update pricing structure status
---

# POST-update-pricing-structure-status

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/pricingStructure/:pricingStructureId/status/:status" %}
{% api-method-summary %}
Update pricing structure status
{% endapi-method-summary %}

{% api-method-description %}
Update pricing structure's status.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="pricingStructureId" type="number" required=true %}
Pricing Structure Id
{% endapi-method-parameter %}

{% api-method-parameter name="status" type="string" required=true %}
Status Code
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
    "message": "Pricing Structure status updated"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



