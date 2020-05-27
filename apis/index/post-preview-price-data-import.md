---
description: Price data import Preview
---

# POST-preview-price-data-import

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/import/prices/preview" %}
{% api-method-summary %}
Price Data Import Preview
{% endapi-method-summary %}

{% api-method-description %}
Preview data for a price data import.
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

{% api-method-query-parameters %}
{% api-method-parameter name="gluten" type="boolean" %}
Whether the cake should be gluten-free or not.
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="priceDataCsvFile" type="object" required=false %}

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
    "type": "PRICE",
    "dataImportId": 6,
    "messages": {
        "infos": [],
        "warnings": [],
        "errors": [
            {
                "title": "Unfound Item",
                "messsage": "Unable to find Item for item format id=15 in view 2"
            },
            {
                "title": "Unfound Item",
                "messsage": "Unable to find Item for item format name=item 3 in view 2"
            }
        ]
    },
    "items": []
 }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



{% hint style="info" %}
* Needs to be `mutiplart/form-data` content-type
* Request body`priceDataCsvFile` attribute is a `multipart/form-dataFile` object
{% endhint %}

