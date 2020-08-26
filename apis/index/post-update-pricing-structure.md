---
description: Update pricing structure
---

# POST-update-pricing-structure

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/pricingStructures" %}
{% api-method-summary %}
Update pricing struture
{% endapi-method-summary %}

{% api-method-description %}
Update a pricing structure.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="pricingStructures" type="array" required=false %}
Pricing Structures JSON Array
{% endapi-method-parameter %}

{% api-method-parameter name="\*.name" type="string" required=false %}
Name
{% endapi-method-parameter %}

{% api-method-parameter name="\*.description" type="string" required=false %}
Description
{% endapi-method-parameter %}

{% api-method-parameter name="\*.viewId" type="number" required=false %}
 View Id
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
  "message": "...." 
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/pricingStructures" %}
{% api-method-summary %}

{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="" type="string" required=false %}

{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```


```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Request body expect a `pricingStructures` attribute of JSON Array containing a `ProcuingStructure` JSON object
{% endhint %}

