---
description: Schedule Item data Import
---

# POST-scedule-item-data-import

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/import/items" %}
{% api-method-summary %}
Schedule Item data import
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
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
Data Import Id
{% endapi-method-parameter %}

{% api-method-parameter name="items" type="array" required=false %}
Items
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
    "id": 3,
    "name": "item-data-import-job-405e9259-fda8-4fc7-b0a0-4292a135384e",
    "description": "item-data-import-job-405e9259-fda8-4fc7-b0a0-4292a135384e description",
    "creationDate": "2020-03-16T04:36:15.000Z",
    "lastUpdate": "2020-03-16T04:36:15.000Z",
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
Request body expect items `attribute` of JSON Array to contains `Attribute` JSON Object.
{% endhint %}

