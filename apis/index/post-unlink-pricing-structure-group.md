# POST-unlink-pricing-structure-group

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/pricing-structure/:pricingStructureId/group/:groupId/unlink" %}
{% api-method-summary %}
Unlink Pricing Structure Group
{% endapi-method-summary %}

{% api-method-description %}
Remove a partner group from a pricing structure.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="groupId" type="number" required=true %}
Group Id
{% endapi-method-parameter %}

{% api-method-parameter name="pricingStructureId" type="number" required=true %}
Pricing Structure Id.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token 
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
    "message": "pricing structure 1 and group 3 unlinked successfully"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



