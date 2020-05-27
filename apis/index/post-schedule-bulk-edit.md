---
description: Schedule bulk edit
---

# POST-schedule-bulk-edit

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/bulk-edit" %}
{% api-method-summary %}
Schedule bulk edit
{% endapi-method-summary %}

{% api-method-description %}
Schedule a bulk edit.
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
{% api-method-parameter name="bulkEditPackage" type="object" required=false %}
Bulk edit package
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
  "message": "....",
  "payload": {
    "id": 1,
    "name": "BulkEditJob-05bb9170-8ded-4fb7-9023-6fff52804a32",
    "creationDate": "2020-03-16T03:57:23.000Z",
    "lastUpdate": "2020-03-16T03:57:23.000Z",
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
Request body expect a `bulkEditPackage` attribute containing a `BulkEditPackage` JSON Object.
{% endhint %}



