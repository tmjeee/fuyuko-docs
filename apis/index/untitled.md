---
description: Heartbeat to determine if application is still alive and responsive
---

# GET-heartbeat

{% api-method method="get" host="http://<host>:<port>/api/v1" path="/heartbeat" %}
{% api-method-summary %}
Heartbeat
{% endapi-method-summary %}

{% api-method-description %}
Get system's heartbeat, this endpoint returns with a timestamp and status of 'SUCCESS' if the application is alive and responsive.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Application is alive and responsive.
{% endapi-method-response-example-description %}

```
{
    "status": "SUCCESS",
    "message": "11-03-2020 05:08:04 pm"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



