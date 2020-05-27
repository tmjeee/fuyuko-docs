---
description: Schedule Pricing Data Import
---

# POST-schedule-pricing-data-import

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/import/prices" %}
{% api-method-summary %}
Schedule pricing data import
{% endapi-method-summary %}

{% api-method-description %}
Schedule a price data import job to run.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="dataImportId" type="number" required=true %}
Data Import ID
{% endapi-method-parameter %}

{% api-method-parameter name="priceDataItems" type="array" required=false %}
Data Items with Price
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
  "message": "....",
  "payload": {
    "id": 4,
    "name": "price-data-import-job-680ffecb-1821-4050-918f-b6969d1d5f3e",
    "description": "price-data-import-job-680ffecb-1821-4050-918f-b6969d1d5f3e description",
    "creationDate": "2020-03-16T04:41:34.000Z",
    "lastUpdate": "2020-03-16T04:41:34.000Z",
    "status": "ENABLED",
    "progress": "SCHEDULED"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Body request expect an attribute `priceDataItems` to be of JSON Array containing `PriceDataItem` JSON Objects.
{% endhint %}



