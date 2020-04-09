---
description: Get all global avatars information
---

# GET-all-global-avatars

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/global/avatars" %}
{% api-method-summary %}
Get all global avatars information
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
All global avatar's information successfully retrieved.
{% endapi-method-response-example-description %}

```
{
  "status": "SUCCESS",
  "message": "....",
  "payload": [
    {
        "id": 1,
        "name": "avatar-01.png",
        "mimeType": "image/png",
        "size": 25843
    },
    {
        "id": 2,
        "name": "avatar-02.png",
        "mimeType": "image/png",
        "size": 22221
    },
    {
        "id": 3,
        "name": "avatar-03.png",
        "mimeType": "image/png",
        "size": 20401
    },
    {
        "id": 4,
        "name": "avatar-04.png",
        "mimeType": "image/png",
        "size": 24003
    },
    {
        "id": 5,
        "name": "avatar-05.png",
        "mimeType": "image/png",
        "size": 18806
    },
    {
        "id": 6,
        "name": "avatar-06.png",
        "mimeType": "image/png",
        "size": 17377
    },
    {
        "id": 7,
        "name": "avatar-07.png",
        "mimeType": "image/png",
        "size": 23136
    },
    {
        "id": 8,
        "name": "avatar-08.png",
        "mimeType": "image/png",
        "size": 23225
    },
    {
        "id": 9,
        "name": "avatar-09.png",
        "mimeType": "image/png",
        "size": 17542
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



