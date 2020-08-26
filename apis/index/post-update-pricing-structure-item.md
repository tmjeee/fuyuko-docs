---
description: Update pricing structure item
---

# POST-update-pricing-structure-item

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/pricingStructure/:pricingStructureId/item" %}
{% api-method-summary %}
Update pricing structure item
{% endapi-method-summary %}

{% api-method-description %}
Update price of an item in a pricing structure.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="pricingStructureId" type="string" required=true %}
Pricing Structure Id.
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="\*.itemId" type="number" required=true %}
Item Id
{% endapi-method-parameter %}

{% api-method-parameter name="\*.price" type="number" required=true %}
Item Price
{% endapi-method-parameter %}

{% api-method-parameter name="\*.country" type="string" required=true %}
Item Country
{% endapi-method-parameter %}

{% api-method-parameter name="pricingStructureItems" type="array" required=true %}
Pricing Structure Items
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
    "message": "Pricing updated"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Body of request expect a `pricingStructureItems` of JSON array to contains `PricingStructureItemWithPrice` JSON object
{% endhint %}

