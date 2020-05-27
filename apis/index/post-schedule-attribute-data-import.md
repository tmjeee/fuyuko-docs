---
description: Schedule attribute data import
---

# POST-schedule-attribute-data-import

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/import/attributes" %}
{% api-method-summary %}
Schedule attribute data import
{% endapi-method-summary %}

{% api-method-description %}
Schedule an attribute data import.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View ID.
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

{% api-method-parameter name="attributes" type="array" required=true %}
Attributes
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
    "id": 2,
    "name": "attribute-data-import-job-22d55815-2073-4979-9e18-a0605f36fbae",
    "description": "attribute-data-import-job-22d55815-2073-4979-9e18-a0605f36fbae description",
    "creationDate": "2020-03-16T04:30:17.000Z",
    "lastUpdate": "2020-03-16T04:30:17.000Z",
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
Request body `attributes` attribute expect a JSON Array containing `Attribute` JSON object.
{% endhint %}

