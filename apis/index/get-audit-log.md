# GET-audit-log

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/audit-log" %}
{% api-method-summary %}
Get Audit Logs
{% endapi-method-summary %}

{% api-method-description %}
Retrieve system's audit logs.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="userId" type="number" required=false %}
userId to filter the audit logs by.
{% endapi-method-parameter %}

{% api-method-parameter name="category" type="string" required=false %}
category to filter the audit logs by.
{% endapi-method-parameter %}

{% api-method-parameter name="level" type="string" required=false %}
Level to filter the audit logs by.
{% endapi-method-parameter %}

{% api-method-parameter name="logs" type="string" required=false %}
logs to filter the results by.
{% endapi-method-parameter %}

{% api-method-parameter name="limit" type="number" %}
Limit for pagination.
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="number" %}
Offset for pagination.
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
    "message": "audit logs retrived",
    "payload": [
        {
            "id": 597,
            "creationDate": "2020-06-04T09:42:04.000Z",
            "lastUpdate": "2020-06-04T09:42:04.000Z",
            "requestUuid": "58d271ed-4ff2-49d6-9aed-1c80d893be17",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=100&offset=0&userId=&category=&level=&logs="
        },
        {
            "id": 596,
            "creationDate": "2020-06-04T09:42:01.000Z",
            "lastUpdate": "2020-06-04T09:42:01.000Z",
            "requestUuid": null,
            "userId": null,
            "userName": null,
            "log": "POST-/api/v1/login"
        },
        {
            "id": 595,
            "creationDate": "2020-06-04T09:41:57.000Z",
            "lastUpdate": "2020-06-04T09:41:57.000Z",
            "requestUuid": null,
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/audit-log?limit=100&offset=0&userId=&category=&level=&logs="
        },
        {
            "id": 588,
            "creationDate": "2020-06-04T09:41:46.000Z",
            "lastUpdate": "2020-06-04T09:41:46.000Z",
            "requestUuid": "5be80cf8-fef9-4dc2-8003-5b209b3a98a6",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 589,
            "creationDate": "2020-06-04T09:41:46.000Z",
            "lastUpdate": "2020-06-04T09:41:46.000Z",
            "requestUuid": "ef4e51a0-2577-473c-a095-8f111437696b",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 590,
            "creationDate": "2020-06-04T09:41:46.000Z",
            "lastUpdate": "2020-06-04T09:41:46.000Z",
            "requestUuid": "6456542a-5252-415b-81b3-f26a5155d941",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 591,
            "creationDate": "2020-06-04T09:41:46.000Z",
            "lastUpdate": "2020-06-04T09:41:46.000Z",
            "requestUuid": "718fc7c6-d4fd-4f7d-841f-332380de3ae0",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 592,
            "creationDate": "2020-06-04T09:41:46.000Z",
            "lastUpdate": "2020-06-04T09:41:46.000Z",
            "requestUuid": "310b5502-b7db-4194-925c-80f7792e34d8",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 593,
            "creationDate": "2020-06-04T09:41:46.000Z",
            "lastUpdate": "2020-06-04T09:41:46.000Z",
            "requestUuid": "c0392b55-1111-401f-b11d-a163b96708a0",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0"
        },
        {
            "id": 594,
            "creationDate": "2020-06-04T09:41:46.000Z",
            "lastUpdate": "2020-06-04T09:41:46.000Z",
            "requestUuid": "9dc33630-fdde-436b-a65d-3be4513a89ee",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.38780315732105497"
        },
        {
            "id": 581,
            "creationDate": "2020-06-04T09:36:05.000Z",
            "lastUpdate": "2020-06-04T09:36:05.000Z",
            "requestUuid": "51e0f38d-025c-4d42-9007-5f0b274877c9",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 582,
            "creationDate": "2020-06-04T09:36:05.000Z",
            "lastUpdate": "2020-06-04T09:36:05.000Z",
            "requestUuid": "047386d4-4b23-4e39-befa-2314c1957e61",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 583,
            "creationDate": "2020-06-04T09:36:05.000Z",
            "lastUpdate": "2020-06-04T09:36:05.000Z",
            "requestUuid": "83209247-a45a-4394-9f2e-9333afa90928",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 584,
            "creationDate": "2020-06-04T09:36:05.000Z",
            "lastUpdate": "2020-06-04T09:36:05.000Z",
            "requestUuid": "eebc7fdc-069d-4a6e-a8b8-461c2d1cc02b",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 585,
            "creationDate": "2020-06-04T09:36:05.000Z",
            "lastUpdate": "2020-06-04T09:36:05.000Z",
            "requestUuid": "6d0e0e40-293a-4765-878e-42b305085860",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 586,
            "creationDate": "2020-06-04T09:36:05.000Z",
            "lastUpdate": "2020-06-04T09:36:05.000Z",
            "requestUuid": "4584c003-3cea-4833-a02f-144bedd1e98e",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0"
        },
        {
            "id": 587,
            "creationDate": "2020-06-04T09:36:05.000Z",
            "lastUpdate": "2020-06-04T09:36:05.000Z",
            "requestUuid": "44c390a0-8465-441e-8770-53f1c6780a33",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.5816726917443873"
        },
        {
            "id": 574,
            "creationDate": "2020-06-04T09:32:06.000Z",
            "lastUpdate": "2020-06-04T09:32:06.000Z",
            "requestUuid": "df527d1c-f72e-4cfd-ac8e-812683fa7979",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 575,
            "creationDate": "2020-06-04T09:32:06.000Z",
            "lastUpdate": "2020-06-04T09:32:06.000Z",
            "requestUuid": "35fec46c-c861-4dfe-9475-5a2f151f0605",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 576,
            "creationDate": "2020-06-04T09:32:06.000Z",
            "lastUpdate": "2020-06-04T09:32:06.000Z",
            "requestUuid": "09771a92-100f-45df-a0c2-218e49241469",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 577,
            "creationDate": "2020-06-04T09:32:06.000Z",
            "lastUpdate": "2020-06-04T09:32:06.000Z",
            "requestUuid": "f6b1903d-b527-4214-bc47-bd86d4aa08ae",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 578,
            "creationDate": "2020-06-04T09:32:06.000Z",
            "lastUpdate": "2020-06-04T09:32:06.000Z",
            "requestUuid": "752a0e05-961d-4e45-9f9f-0525f8cfa733",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 579,
            "creationDate": "2020-06-04T09:32:06.000Z",
            "lastUpdate": "2020-06-04T09:32:06.000Z",
            "requestUuid": "4e67c9ff-8076-45d0-b23c-9079a84ecb24",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0"
        },
        {
            "id": 580,
            "creationDate": "2020-06-04T09:32:06.000Z",
            "lastUpdate": "2020-06-04T09:32:06.000Z",
            "requestUuid": "9dad24f3-78b0-4cb0-ba40-93b4475a6076",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.04778102049379607"
        },
        {
            "id": 567,
            "creationDate": "2020-06-04T09:30:45.000Z",
            "lastUpdate": "2020-06-04T09:30:45.000Z",
            "requestUuid": "8530e24d-2292-4310-a3dd-1a87d0527ef4",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 568,
            "creationDate": "2020-06-04T09:30:45.000Z",
            "lastUpdate": "2020-06-04T09:30:45.000Z",
            "requestUuid": "cedbc14e-12af-4825-aa3a-5c901991176e",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 569,
            "creationDate": "2020-06-04T09:30:45.000Z",
            "lastUpdate": "2020-06-04T09:30:45.000Z",
            "requestUuid": "6d159edb-3a3d-4853-9fb0-fb56a855caff",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 570,
            "creationDate": "2020-06-04T09:30:45.000Z",
            "lastUpdate": "2020-06-04T09:30:45.000Z",
            "requestUuid": "767b6f98-a6f0-4e11-b961-36d265a1d899",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 571,
            "creationDate": "2020-06-04T09:30:45.000Z",
            "lastUpdate": "2020-06-04T09:30:45.000Z",
            "requestUuid": "7523dd83-582e-4540-ab91-c49dbb0d4fa5",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 572,
            "creationDate": "2020-06-04T09:30:45.000Z",
            "lastUpdate": "2020-06-04T09:30:45.000Z",
            "requestUuid": "0c6f0ead-849f-4cff-8241-8c9293d0f044",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0"
        },
        {
            "id": 573,
            "creationDate": "2020-06-04T09:30:45.000Z",
            "lastUpdate": "2020-06-04T09:30:45.000Z",
            "requestUuid": "9b4163a2-e24f-49af-8d06-0460227b92c3",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.4295273173470624"
        },
        {
            "id": 561,
            "creationDate": "2020-06-04T09:29:42.000Z",
            "lastUpdate": "2020-06-04T09:29:42.000Z",
            "requestUuid": "b86b7d61-6534-4464-8785-b87be29cbffa",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 562,
            "creationDate": "2020-06-04T09:29:42.000Z",
            "lastUpdate": "2020-06-04T09:29:42.000Z",
            "requestUuid": "0382b434-ac4b-40ce-aca2-6e2137b3b0b9",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 563,
            "creationDate": "2020-06-04T09:29:42.000Z",
            "lastUpdate": "2020-06-04T09:29:42.000Z",
            "requestUuid": "875bda79-8dad-49d0-b8ff-1930f9702c57",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 564,
            "creationDate": "2020-06-04T09:29:42.000Z",
            "lastUpdate": "2020-06-04T09:29:42.000Z",
            "requestUuid": "a33e4f8f-de7f-4fc6-8246-6da9e1c3ccfe",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 565,
            "creationDate": "2020-06-04T09:29:42.000Z",
            "lastUpdate": "2020-06-04T09:29:42.000Z",
            "requestUuid": "756f5f30-4d8e-462f-a995-3f89ae64f2d6",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 566,
            "creationDate": "2020-06-04T09:29:42.000Z",
            "lastUpdate": "2020-06-04T09:29:42.000Z",
            "requestUuid": "12fab208-7478-4540-8c6c-0763a9489b04",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.2942603984137062"
        },
        {
            "id": 555,
            "creationDate": "2020-06-04T09:29:28.000Z",
            "lastUpdate": "2020-06-04T09:29:28.000Z",
            "requestUuid": "48c8f3eb-e950-4f25-8c38-fac7fbe60dd9",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 556,
            "creationDate": "2020-06-04T09:29:28.000Z",
            "lastUpdate": "2020-06-04T09:29:28.000Z",
            "requestUuid": "240c62a1-512b-4cbf-84ea-9b9c5eb8a5ac",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 557,
            "creationDate": "2020-06-04T09:29:28.000Z",
            "lastUpdate": "2020-06-04T09:29:28.000Z",
            "requestUuid": "6e243b06-0f52-40ad-92de-4e4196676f1e",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 558,
            "creationDate": "2020-06-04T09:29:28.000Z",
            "lastUpdate": "2020-06-04T09:29:28.000Z",
            "requestUuid": "ad0e4cd1-6bc9-4f94-8fc3-b8a949526763",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 559,
            "creationDate": "2020-06-04T09:29:28.000Z",
            "lastUpdate": "2020-06-04T09:29:28.000Z",
            "requestUuid": "a1b39b51-9345-4f9c-bd5e-94109bad2f06",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 560,
            "creationDate": "2020-06-04T09:29:28.000Z",
            "lastUpdate": "2020-06-04T09:29:28.000Z",
            "requestUuid": "36ab8396-5d78-4657-8b8a-91e24dbc949e",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.7222412696571527"
        },
        {
            "id": 553,
            "creationDate": "2020-06-04T09:28:20.000Z",
            "lastUpdate": "2020-06-04T09:28:20.000Z",
            "requestUuid": "2c39c0bd-20a4-4cd3-832d-b580759b4f9a",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0%20&userId=4&logs=aasdsd"
        },
        {
            "id": 554,
            "creationDate": "2020-06-04T09:28:20.000Z",
            "lastUpdate": "2020-06-04T09:28:20.000Z",
            "requestUuid": "532fc25b-78ad-45cf-9781-fcb729938ad2",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/search/status/ENABLED/user/[object%20Object]"
        },
        {
            "id": 552,
            "creationDate": "2020-06-04T09:28:17.000Z",
            "lastUpdate": "2020-06-04T09:28:17.000Z",
            "requestUuid": "7803297a-f5a2-4ea2-bff9-05c5af0ae5b9",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/search/status/ENABLED/user/s"
        },
        {
            "id": 551,
            "creationDate": "2020-06-04T09:28:11.000Z",
            "lastUpdate": "2020-06-04T09:28:11.000Z",
            "requestUuid": "400d22ad-9417-4a3d-8160-3e42de712d37",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0%20&logs=aasdsd"
        },
        {
            "id": 550,
            "creationDate": "2020-06-04T09:27:57.000Z",
            "lastUpdate": "2020-06-04T09:27:57.000Z",
            "requestUuid": "bf2a49b8-5df6-4c68-b018-af470c5a9bad",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0"
        },
        {
            "id": 548,
            "creationDate": "2020-06-04T09:27:56.000Z",
            "lastUpdate": "2020-06-04T09:27:56.000Z",
            "requestUuid": "2bc171a9-f192-40f3-b18c-5f6f20c9dd71",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0"
        },
        {
            "id": 549,
            "creationDate": "2020-06-04T09:27:56.000Z",
            "lastUpdate": "2020-06-04T09:27:56.000Z",
            "requestUuid": "82a8b3c2-f580-4672-ba6d-c7918041ebca",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0"
        },
        {
            "id": 547,
            "creationDate": "2020-06-04T09:27:54.000Z",
            "lastUpdate": "2020-06-04T09:27:54.000Z",
            "requestUuid": "d1cd08de-987f-4a43-9259-bba9b26c7e4c",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0"
        },
        {
            "id": 546,
            "creationDate": "2020-06-04T09:26:31.000Z",
            "lastUpdate": "2020-06-04T09:26:31.000Z",
            "requestUuid": "37f6fa0c-9fdf-429e-ad5a-43b8eab8880a",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=50&offset=0"
        },
        {
            "id": 542,
            "creationDate": "2020-06-04T09:26:29.000Z",
            "lastUpdate": "2020-06-04T09:26:29.000Z",
            "requestUuid": "de536157-4d82-47c1-b7ba-ebdc8c02ee05",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 543,
            "creationDate": "2020-06-04T09:26:29.000Z",
            "lastUpdate": "2020-06-04T09:26:29.000Z",
            "requestUuid": "8837996d-508e-4d7f-ac92-7e5cf81c44f1",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 544,
            "creationDate": "2020-06-04T09:26:29.000Z",
            "lastUpdate": "2020-06-04T09:26:29.000Z",
            "requestUuid": "13b87579-69a8-47d2-baee-c1d997124732",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 545,
            "creationDate": "2020-06-04T09:26:29.000Z",
            "lastUpdate": "2020-06-04T09:26:29.000Z",
            "requestUuid": "f183630d-0cc2-4b47-8454-6f77dcc25a48",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.3341902848246996"
        },
        {
            "id": 540,
            "creationDate": "2020-06-04T09:26:26.000Z",
            "lastUpdate": "2020-06-04T09:26:26.000Z",
            "requestUuid": "4b9b7b9b-a8dd-4b69-8e9c-d04820d06421",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 541,
            "creationDate": "2020-06-04T09:26:26.000Z",
            "lastUpdate": "2020-06-04T09:26:26.000Z",
            "requestUuid": "e1a1f4a9-5688-4077-9815-e0d364d78f97",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 539,
            "creationDate": "2020-06-04T09:25:48.000Z",
            "lastUpdate": "2020-06-04T09:25:48.000Z",
            "requestUuid": "26f6d2b0-4f0a-431e-88d8-c4e176e2484d",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/audit-log?limit=100&offset=0"
        },
        {
            "id": 535,
            "creationDate": "2020-06-04T09:25:10.000Z",
            "lastUpdate": "2020-06-04T09:25:10.000Z",
            "requestUuid": "51697a41-4def-44c7-ac8d-0b2a1561e929",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 536,
            "creationDate": "2020-06-04T09:25:10.000Z",
            "lastUpdate": "2020-06-04T09:25:10.000Z",
            "requestUuid": "3d0d80c7-cb69-4c1b-bdf1-41121a7aeb3b",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 537,
            "creationDate": "2020-06-04T09:25:10.000Z",
            "lastUpdate": "2020-06-04T09:25:10.000Z",
            "requestUuid": "e1485ed3-6051-4511-b217-b86111d79162",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 538,
            "creationDate": "2020-06-04T09:25:10.000Z",
            "lastUpdate": "2020-06-04T09:25:10.000Z",
            "requestUuid": "1f6a3b03-485a-4e86-813d-107748abbf9c",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.3160884764833305"
        },
        {
            "id": 525,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": null,
            "userId": null,
            "userName": null,
            "log": "POST-/api/v1/login"
        },
        {
            "id": 526,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": "9237e1d8-e93a-428b-b5e0-d5fd7ffb9f64",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 527,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": "b0b20d6a-4d91-4204-ba51-b6013d1655bc",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 528,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": "ee55f7f4-c518-4691-b603-0f820462f0f6",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 529,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": "c0e298b8-8dcc-417c-bcad-91bba677ed06",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 530,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": "6952bdd3-9239-47cd-947f-2eb1c550b863",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 531,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": "ab506ceb-3578-4bd9-b0b3-d90d143c60ea",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 532,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": "cc8d9977-7512-48e5-b1fe-b3ca2f92f59c",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_DASHBOARD.md"
        },
        {
            "id": 533,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": "4c1794ac-9018-4582-bb01-7c3fe92d1e1e",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/dashboard"
        },
        {
            "id": 534,
            "creationDate": "2020-06-04T09:25:07.000Z",
            "lastUpdate": "2020-06-04T09:25:07.000Z",
            "requestUuid": "93e59d46-718f-4fdb-9a83-c2ca4f8b13d5",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.12700879228854145"
        },
        {
            "id": 521,
            "creationDate": "2020-06-04T09:24:58.000Z",
            "lastUpdate": "2020-06-04T09:24:58.000Z",
            "requestUuid": null,
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 522,
            "creationDate": "2020-06-04T09:24:58.000Z",
            "lastUpdate": "2020-06-04T09:24:58.000Z",
            "requestUuid": null,
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/views"
        },
        {
            "id": 523,
            "creationDate": "2020-06-04T09:24:58.000Z",
            "lastUpdate": "2020-06-04T09:24:58.000Z",
            "requestUuid": null,
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 524,
            "creationDate": "2020-06-04T09:24:58.000Z",
            "lastUpdate": "2020-06-04T09:24:58.000Z",
            "requestUuid": null,
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 515,
            "creationDate": "2020-06-04T07:08:51.000Z",
            "lastUpdate": "2020-06-04T07:08:51.000Z",
            "requestUuid": "291e33e6-7ff3-4ca5-b4d0-9ce1de525cf8",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 516,
            "creationDate": "2020-06-04T07:08:51.000Z",
            "lastUpdate": "2020-06-04T07:08:51.000Z",
            "requestUuid": "2d8dbee2-c3c0-4422-a664-f552bdaeffd9",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 517,
            "creationDate": "2020-06-04T07:08:51.000Z",
            "lastUpdate": "2020-06-04T07:08:51.000Z",
            "requestUuid": "89aad8b1-e4d9-463c-be36-498b8d770bf5",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 518,
            "creationDate": "2020-06-04T07:08:51.000Z",
            "lastUpdate": "2020-06-04T07:08:51.000Z",
            "requestUuid": "e8638536-d53e-4ed9-a95c-a0934d5d7f3e",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 519,
            "creationDate": "2020-06-04T07:08:51.000Z",
            "lastUpdate": "2020-06-04T07:08:51.000Z",
            "requestUuid": "dfd022ac-81a9-43c9-8668-ca88648584c3",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 520,
            "creationDate": "2020-06-04T07:08:51.000Z",
            "lastUpdate": "2020-06-04T07:08:51.000Z",
            "requestUuid": "dbb9d225-4a11-4fd9-b461-f650bd278c74",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.6559102312228311"
        },
        {
            "id": 512,
            "creationDate": "2020-06-04T06:54:55.000Z",
            "lastUpdate": "2020-06-04T06:54:55.000Z",
            "requestUuid": "64cfd840-1600-4b40-9299-01c540427a89",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 513,
            "creationDate": "2020-06-04T06:54:55.000Z",
            "lastUpdate": "2020-06-04T06:54:55.000Z",
            "requestUuid": "4c17ac52-569e-47bd-ba2b-480ff03c4027",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 514,
            "creationDate": "2020-06-04T06:54:55.000Z",
            "lastUpdate": "2020-06-04T06:54:55.000Z",
            "requestUuid": "3231031c-f9f4-4b8c-bcf5-6e2c94cf3360",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.5548662002102052"
        },
        {
            "id": 509,
            "creationDate": "2020-06-04T06:54:55.000Z",
            "lastUpdate": "2020-06-04T06:54:55.000Z",
            "requestUuid": "883e9ec3-06dd-4b5f-ba64-0ac5ca86fa7d",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 510,
            "creationDate": "2020-06-04T06:54:55.000Z",
            "lastUpdate": "2020-06-04T06:54:55.000Z",
            "requestUuid": "79b9661b-3e22-417c-b28b-170ccdc01edb",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 511,
            "creationDate": "2020-06-04T06:54:55.000Z",
            "lastUpdate": "2020-06-04T06:54:55.000Z",
            "requestUuid": "560c0ce5-83c3-43b7-9022-1b767e818056",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 508,
            "creationDate": "2020-06-04T06:54:26.000Z",
            "lastUpdate": "2020-06-04T06:54:26.000Z",
            "requestUuid": "d77b712c-6351-4045-8103-e9e787dc1025",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.22013654020340834"
        },
        {
            "id": 503,
            "creationDate": "2020-06-04T06:54:25.000Z",
            "lastUpdate": "2020-06-04T06:54:25.000Z",
            "requestUuid": "c4c64f14-0657-42b8-917e-05f20c5e4e1c",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 504,
            "creationDate": "2020-06-04T06:54:25.000Z",
            "lastUpdate": "2020-06-04T06:54:25.000Z",
            "requestUuid": "a53365b1-6692-432d-bf73-4381ebe8fbb0",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/views"
        },
        {
            "id": 505,
            "creationDate": "2020-06-04T06:54:25.000Z",
            "lastUpdate": "2020-06-04T06:54:25.000Z",
            "requestUuid": "9ae8e3ff-0471-4294-93a3-8f2a00694557",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 506,
            "creationDate": "2020-06-04T06:54:25.000Z",
            "lastUpdate": "2020-06-04T06:54:25.000Z",
            "requestUuid": "e9a5509c-23de-4145-9a2c-1a956bcc61ab",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 507,
            "creationDate": "2020-06-04T06:54:25.000Z",
            "lastUpdate": "2020-06-04T06:54:25.000Z",
            "requestUuid": "5999dfb2-5c64-4f48-bca9-df649135d521",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 499,
            "creationDate": "2020-06-04T06:52:56.000Z",
            "lastUpdate": "2020-06-04T06:52:56.000Z",
            "requestUuid": "7a9232dd-0ca2-45bb-8277-36efd80c3b29",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        },
        {
            "id": 500,
            "creationDate": "2020-06-04T06:52:56.000Z",
            "lastUpdate": "2020-06-04T06:52:56.000Z",
            "requestUuid": "168819fa-828a-49dc-b275-2af572972b85",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/notifications"
        },
        {
            "id": 501,
            "creationDate": "2020-06-04T06:52:56.000Z",
            "lastUpdate": "2020-06-04T06:52:56.000Z",
            "requestUuid": "1703152d-69bd-478e-b72c-e16c71e34859",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/help/HELP_ADMINISTRATION.md"
        },
        {
            "id": 502,
            "creationDate": "2020-06-04T06:52:56.000Z",
            "lastUpdate": "2020-06-04T06:52:56.000Z",
            "requestUuid": "ee906417-c08b-494d-bf5b-d7a890c834af",
            "userId": null,
            "userName": null,
            "log": "GET-/api/v1/user/2/avatar?=0.04180821822066316"
        },
        {
            "id": 497,
            "creationDate": "2020-06-04T06:52:55.000Z",
            "lastUpdate": "2020-06-04T06:52:55.000Z",
            "requestUuid": "7b8c61e4-ad9f-454a-b30a-d1ca7e858150",
            "userId": 2,
            "userName": "cypress",
            "log": "GET-/api/v1/user/2/settings"
        }
    ],
    "limit": 100,
    "offset": 0,
    "total": 596
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Possible Category values are 

* SYSTEM
* APP
* USER
* HTTP
{% endhint %}

{% hint style="info" %}
Possible Level values are 

* DEBUG
* INFO
* WARN
* ERROR
{% endhint %}

