---
description: Custom export preview
---

# POST-custom-export-preview

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/custom-export/:customExportId/preview" %}
{% api-method-summary %}
Custom Export Preview
{% endapi-method-summary %}

{% api-method-description %}
Preview a custom export.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
{% endapi-method-parameter %}

{% api-method-parameter name="customExportId" type="number" required=true %}
Custom Export Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="values" type="array" required=true %}

{% endapi-method-parameter %}

{% api-method-parameter name="values.\*.name" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="values.\*.type" type="string" required=false %}

{% endapi-method-parameter %}

{% api-method-parameter name="values.\*.value" type="string" required=false %}

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
  "message": "...",
  "payload":{
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

{% hint style="info" %}
`values` is expected to be a `JSON Array` containing object with `name`, `type` and `value` properties
{% endhint %}



