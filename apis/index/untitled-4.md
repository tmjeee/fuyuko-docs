---
description: Get all jobs
---

# GET-all-jobs

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/jobs" %}
{% api-method-summary %}
Get all jobs
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
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
[
    {
        "id": 1,
        "name": "BulkEditJob-05bb9170-8ded-4fb7-9023-6fff52804a32",
        "description": "Bulk Edit Job (05bb9170-8ded-4fb7-9023-6fff52804a32) for viewId 1",
        "creationDate": "2020-03-16T03:57:23.000Z",
        "lastUpdate": "2020-03-16T03:57:23.000Z",
        "status": "ENABLED",
        "progress": "COMPLETED"
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



