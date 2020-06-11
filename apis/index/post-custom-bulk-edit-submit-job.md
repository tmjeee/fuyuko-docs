# POST-custom-bulk-edit-submit-job

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/custom-bulk-edit/:customBulkEditId/submit-job" %}
{% api-method-summary %}
Get Cakes
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

{% api-method-parameter name="customBulkEditId" type="number" required=true %}
Custom Bulk Edit ID
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
    "message": "Export script job submission done",
    "payload": {
        "valid": true,
        "messages": [
            {
                "status": "INFO",
                "title": "Success",
                "message": "Custom bulk edit job 0.0.1-sample-custom-bulk-edit-1.js-9a276e87-c918-4588-8438-9475856381da submitted"
            }
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



