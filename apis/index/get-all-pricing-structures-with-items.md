---
description: Get all pricing structures and its items
---

# GET-all-pricing-structures-with-items

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/pricingStructuresWithItems/:pricingStructureId" %}
{% api-method-summary %}
All Pricing Structures and its items
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="pricingStructureId" type="number" required=true %}
Pricing Structure Id .
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="number" required=false %}
limit for pagination, greater than zero
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="number" required=false %}
offset for pagniation, zero or greater
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
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
    "id": 1,
    "name": "Pricing Structure #1",
    "viewId": 1,
    "description": "Pricing Structure #1 Description",
    "items": {
      "limit": 10,
      "offset": 0,
      "total": 200,
      "payload": [
        {
            "id": 1,
            "itemId": 1,
            "itemName": "name xxx",
            "itemDescription": "description xxx",
            "parentId": null,
            "country": "AUD",
            "price": 2.23,
            "children": [
                {
                    "id": 2,
                    "itemId": 2,
                    "itemName": "Item-1-1",
                    "itemDescription": "Item-1-1 Description",
                    "price": 10.04,
                    "country": "AUD",
                    "parentId": 1,
                    "children": []
                },
                {
                    "id": 3,
                    "itemId": 3,
                    "itemName": "Item-1-2",
                    "itemDescription": "Item-1-2 Description",
                    "price": 6.69,
                    "country": "AUD",
                    "parentId": 1,
                    "children": []
                }
            ]
        },
        {
            "id": 4,
            "itemId": 4,
            "itemName": "Item-2",
            "itemDescription": "Item-2 Description",
            "parentId": null,
            "country": "AUD",
            "price": 3.42,
            "children": []
        },
        {
            "id": 5,
            "itemId": 5,
            "itemName": "Item-3",
            "itemDescription": "Item-3 Description",
            "parentId": null,
            "country": "AUD",
            "price": 5.96,
            "children": []
        },
        {
            "id": 6,
            "itemId": 6,
            "itemName": "Item-4",
            "itemDescription": "Item-4 Description",
            "parentId": null,
            "country": "AUD",
            "price": 8.75,
            "children": []
        },
        {
            "id": 7,
            "itemId": 7,
            "itemName": "Item-5",
            "itemDescription": "Item-5 Description",
            "parentId": null,
            "country": "AUD",
            "price": 5.71,
            "children": []
        },
        {
            "id": 8,
            "itemId": 8,
            "itemName": "Item-6",
            "itemDescription": "Item-6 Description",
            "parentId": null,
            "country": "AUD",
            "price": 8.98,
            "children": []
        },
        {
            "id": 9,
            "itemId": 9,
            "itemName": "Item-7",
            "itemDescription": "Item-7 Description",
            "parentId": null,
            "country": "AUD",
            "price": 9.39,
            "children": []
        }
    ]}
  }
 }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



