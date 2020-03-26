---
description: Get exported file by Id
---

# GET-export-file-by-id

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/export/:exportDataId/file" %}
{% api-method-summary %}
Get exported file by Id
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="exportDataId" type="string" required=true %}
Export Data Id.
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
"id","name","description","string attribute","text attribute"
1,"Item-1","Item-1 Description","some string 154","some text 25027"
4,"Item-2","Item-2 Description","some string 18598","some text 28828"
5,"Item-3","Item-3 Description","some string 85614","some text 30460"
6,"Item-4","Item-4 Description","some string 45119","some text 38135"
7,"Item-5","Item-5 Description","some string 12687","some text 21223"
8,"Item-6","Item-6 Description","some string 16862","some text 77974"
9,"Item-7","Item-7 Description","some string 43314","some text 99952"
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
The response is in whatever format the data export artifact is in. In this case it is t`ext/csv`
{% endhint %}



