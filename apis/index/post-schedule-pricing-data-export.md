---
description: Schedule Pricing Data Export
---

# POST-schedule-pricing-data-export

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/export/pricingStructure/:pricingStructureId/prices" %}
{% api-method-summary %}
Schedule pricing data export
{% endapi-method-summary %}

{% api-method-description %}
Schedule a pricing data export job.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="string" required=true %}
View ID
{% endapi-method-parameter %}

{% api-method-parameter name="pricingStructureId" type="string" required=true %}
Pricing Structure ID.
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
  "message": "....",
  "payload": {
    "id": 8,
    "name": "price-data-export-job-3566e567-e601-434e-9807-7cfcf0c36cf6",
    "description": "price-data-export-job-3566e567-e601-434e-9807-7cfcf0c36cf6 description",
    "creationDate": "2020-03-25T09:43:29.000Z",
    "lastUpdate": "2020-03-25T09:43:29.000Z",
    "status": "ENABLED",
    "progress": "SCHEDULED"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



