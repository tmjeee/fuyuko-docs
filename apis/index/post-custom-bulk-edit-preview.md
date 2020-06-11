# POST-custom-bulk-edit-preview

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/custom-bulk-edit/:customBulkEditId/preview" %}
{% api-method-summary %}
Preview custom bulk edit
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
Custom bulk edit ID.
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
    "message": "Import script preview ready",
    "payload": {
        "proceed": true,
        "messages": [
            {
                "status": "INFO",
                "title": "test",
                "message": "test message"
            }
        ],
        "columns": [
            "column1",
            "column2",
            "column3"
        ],
        "rows": [
            {
                "column1": "row1 column1",
                "column2": "row1 column2",
                "column3": "row1 column3"
            },
            {
                "column1": "row2 column1",
                "column2": "row2 column2",
                "column3": "row2 column3"
            },
            {
                "column1": "row3 column1",
                "column2": "row3 column2",
                "column3": "row3 column3"
            }
        ]
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



