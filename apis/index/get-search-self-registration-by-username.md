---
description: Search self registration by username
---

# GET-search-self-registration-by-username

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/search/self-registration/:username" %}
{% api-method-summary %}
Search self registration by username
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
Username to search for
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
  "message": "....",
  "payload": [
    {
        "id": 1,
        "username": "self1",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self1-lastname",
        "firstName": "self1-firstname",
        "email": "self1@gmail.com"
    },
    {
        "id": 2,
        "username": "self2",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self2-lastname",
        "firstName": "self2-firstname",
        "email": "self2@gmail.com"
    },
    {
        "id": 3,
        "username": "self3",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self3-lastname",
        "firstName": "self3-firstname",
        "email": "self3@gmail.com"
    },
    {
        "id": 4,
        "username": "self4",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self4-lastname",
        "firstName": "self4-firstname",
        "email": "self4@gmail.com"
    },
    {
        "id": 5,
        "username": "self5",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self5-lastname",
        "firstName": "self5-firstname",
        "email": "self5@gmail.com"
    },
    {
        "id": 6,
        "username": "self6",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self6-lastname",
        "firstName": "self6-firstname",
        "email": "self6@gmail.com"
    },
    {
        "id": 7,
        "username": "self7",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self7-lastname",
        "firstName": "self7-firstname",
        "email": "self7@gmail.com"
    },
    {
        "id": 8,
        "username": "self8",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self8-lastname",
        "firstName": "self8-firstname",
        "email": "self8@gmail.com"
    },
    {
        "id": 9,
        "username": "self9",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self9-lastname",
        "firstName": "self9-firstname",
        "email": "self9@gmail.com"
    },
    {
        "id": 10,
        "username": "self10",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self10-lastname",
        "firstName": "self10-firstname",
        "email": "self10@gmail.com"
    },
    {
        "id": 11,
        "username": "self11",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self11-lastname",
        "firstName": "self11-firstname",
        "email": "self11@gmail.com"
    },
    {
        "id": 12,
        "username": "self12",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self12-lastname",
        "firstName": "self12-firstname",
        "email": "self12@gmail.com"
    },
    {
        "id": 13,
        "username": "self13",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self13-lastname",
        "firstName": "self13-firstname",
        "email": "self13@gmail.com"
    },
    {
        "id": 14,
        "username": "self14",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self14-lastname",
        "firstName": "self14-firstname",
        "email": "self14@gmail.com"
    },
    {
        "id": 15,
        "username": "self15",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self15-lastname",
        "firstName": "self15-firstname",
        "email": "self15@gmail.com"
    },
    {
        "id": 16,
        "username": "self16",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self16-lastname",
        "firstName": "self16-firstname",
        "email": "self16@gmail.com"
    },
    {
        "id": 17,
        "username": "self17",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self17-lastname",
        "firstName": "self17-firstname",
        "email": "self17@gmail.com"
    },
    {
        "id": 18,
        "username": "self18",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self18-lastname",
        "firstName": "self18-firstname",
        "email": "self18@gmail.com"
    },
    {
        "id": 19,
        "username": "self19",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self19-lastname",
        "firstName": "self19-firstname",
        "email": "self19@gmail.com"
    },
    {
        "id": 20,
        "username": "self20",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self20-lastname",
        "firstName": "self20-firstname",
        "email": "self20@gmail.com"
    },
    {
        "id": 21,
        "username": "self21",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self21-lastname",
        "firstName": "self21-firstname",
        "email": "self21@gmail.com"
    },
    {
        "id": 22,
        "username": "self22",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self22-lastname",
        "firstName": "self22-firstname",
        "email": "self22@gmail.com"
    },
    {
        "id": 23,
        "username": "self23",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self23-lastname",
        "firstName": "self23-firstname",
        "email": "self23@gmail.com"
    },
    {
        "id": 24,
        "username": "self24",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self24-lastname",
        "firstName": "self24-firstname",
        "email": "self24@gmail.com"
    },
    {
        "id": 25,
        "username": "self25",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self25-lastname",
        "firstName": "self25-firstname",
        "email": "self25@gmail.com"
    },
    {
        "id": 26,
        "username": "self26",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self26-lastname",
        "firstName": "self26-firstname",
        "email": "self26@gmail.com"
    },
    {
        "id": 27,
        "username": "self27",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self27-lastname",
        "firstName": "self27-firstname",
        "email": "self27@gmail.com"
    },
    {
        "id": 28,
        "username": "self28",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self28-lastname",
        "firstName": "self28-firstname",
        "email": "self28@gmail.com"
    },
    {
        "id": 29,
        "username": "self29",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self29-lastname",
        "firstName": "self29-firstname",
        "email": "self29@gmail.com"
    },
    {
        "id": 30,
        "username": "self30",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self30-lastname",
        "firstName": "self30-firstname",
        "email": "self30@gmail.com"
    },
    {
        "id": 31,
        "username": "self31",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self31-lastname",
        "firstName": "self31-firstname",
        "email": "self31@gmail.com"
    },
    {
        "id": 32,
        "username": "self32",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self32-lastname",
        "firstName": "self32-firstname",
        "email": "self32@gmail.com"
    },
    {
        "id": 33,
        "username": "self33",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self33-lastname",
        "firstName": "self33-firstname",
        "email": "self33@gmail.com"
    },
    {
        "id": 34,
        "username": "self34",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self34-lastname",
        "firstName": "self34-firstname",
        "email": "self34@gmail.com"
    },
    {
        "id": 35,
        "username": "self35",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self35-lastname",
        "firstName": "self35-firstname",
        "email": "self35@gmail.com"
    },
    {
        "id": 36,
        "username": "self36",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self36-lastname",
        "firstName": "self36-firstname",
        "email": "self36@gmail.com"
    },
    {
        "id": 37,
        "username": "self37",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self37-lastname",
        "firstName": "self37-firstname",
        "email": "self37@gmail.com"
    },
    {
        "id": 38,
        "username": "self38",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self38-lastname",
        "firstName": "self38-firstname",
        "email": "self38@gmail.com"
    },
    {
        "id": 39,
        "username": "self39",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self39-lastname",
        "firstName": "self39-firstname",
        "email": "self39@gmail.com"
    },
    {
        "id": 40,
        "username": "self40",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self40-lastname",
        "firstName": "self40-firstname",
        "email": "self40@gmail.com"
    },
    {
        "id": 41,
        "username": "self41",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self41-lastname",
        "firstName": "self41-firstname",
        "email": "self41@gmail.com"
    },
    {
        "id": 42,
        "username": "self42",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self42-lastname",
        "firstName": "self42-firstname",
        "email": "self42@gmail.com"
    },
    {
        "id": 43,
        "username": "self43",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self43-lastname",
        "firstName": "self43-firstname",
        "email": "self43@gmail.com"
    },
    {
        "id": 44,
        "username": "self44",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self44-lastname",
        "firstName": "self44-firstname",
        "email": "self44@gmail.com"
    },
    {
        "id": 45,
        "username": "self45",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self45-lastname",
        "firstName": "self45-firstname",
        "email": "self45@gmail.com"
    },
    {
        "id": 46,
        "username": "self46",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self46-lastname",
        "firstName": "self46-firstname",
        "email": "self46@gmail.com"
    },
    {
        "id": 47,
        "username": "self47",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self47-lastname",
        "firstName": "self47-firstname",
        "email": "self47@gmail.com"
    },
    {
        "id": 48,
        "username": "self48",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self48-lastname",
        "firstName": "self48-firstname",
        "email": "self48@gmail.com"
    },
    {
        "id": 49,
        "username": "self49",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self49-lastname",
        "firstName": "self49-firstname",
        "email": "self49@gmail.com"
    },
    {
        "id": 50,
        "username": "self50",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self50-lastname",
        "firstName": "self50-firstname",
        "email": "self50@gmail.com"
    },
    {
        "id": 51,
        "username": "self51",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self51-lastname",
        "firstName": "self51-firstname",
        "email": "self51@gmail.com"
    },
    {
        "id": 52,
        "username": "self52",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self52-lastname",
        "firstName": "self52-firstname",
        "email": "self52@gmail.com"
    },
    {
        "id": 53,
        "username": "self53",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self53-lastname",
        "firstName": "self53-firstname",
        "email": "self53@gmail.com"
    },
    {
        "id": 54,
        "username": "self54",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self54-lastname",
        "firstName": "self54-firstname",
        "email": "self54@gmail.com"
    },
    {
        "id": 55,
        "username": "self55",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self55-lastname",
        "firstName": "self55-firstname",
        "email": "self55@gmail.com"
    },
    {
        "id": 56,
        "username": "self56",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self56-lastname",
        "firstName": "self56-firstname",
        "email": "self56@gmail.com"
    },
    {
        "id": 57,
        "username": "self57",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self57-lastname",
        "firstName": "self57-firstname",
        "email": "self57@gmail.com"
    },
    {
        "id": 58,
        "username": "self58",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self58-lastname",
        "firstName": "self58-firstname",
        "email": "self58@gmail.com"
    },
    {
        "id": 59,
        "username": "self59",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self59-lastname",
        "firstName": "self59-firstname",
        "email": "self59@gmail.com"
    },
    {
        "id": 60,
        "username": "self60",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self60-lastname",
        "firstName": "self60-firstname",
        "email": "self60@gmail.com"
    },
    {
        "id": 61,
        "username": "self61",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self61-lastname",
        "firstName": "self61-firstname",
        "email": "self61@gmail.com"
    },
    {
        "id": 62,
        "username": "self62",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self62-lastname",
        "firstName": "self62-firstname",
        "email": "self62@gmail.com"
    },
    {
        "id": 63,
        "username": "self63",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self63-lastname",
        "firstName": "self63-firstname",
        "email": "self63@gmail.com"
    },
    {
        "id": 64,
        "username": "self64",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self64-lastname",
        "firstName": "self64-firstname",
        "email": "self64@gmail.com"
    },
    {
        "id": 65,
        "username": "self65",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self65-lastname",
        "firstName": "self65-firstname",
        "email": "self65@gmail.com"
    },
    {
        "id": 66,
        "username": "self66",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self66-lastname",
        "firstName": "self66-firstname",
        "email": "self66@gmail.com"
    },
    {
        "id": 67,
        "username": "self67",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self67-lastname",
        "firstName": "self67-firstname",
        "email": "self67@gmail.com"
    },
    {
        "id": 68,
        "username": "self68",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self68-lastname",
        "firstName": "self68-firstname",
        "email": "self68@gmail.com"
    },
    {
        "id": 69,
        "username": "self69",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self69-lastname",
        "firstName": "self69-firstname",
        "email": "self69@gmail.com"
    },
    {
        "id": 70,
        "username": "self70",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self70-lastname",
        "firstName": "self70-firstname",
        "email": "self70@gmail.com"
    },
    {
        "id": 71,
        "username": "self71",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self71-lastname",
        "firstName": "self71-firstname",
        "email": "self71@gmail.com"
    },
    {
        "id": 72,
        "username": "self72",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self72-lastname",
        "firstName": "self72-firstname",
        "email": "self72@gmail.com"
    },
    {
        "id": 73,
        "username": "self73",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self73-lastname",
        "firstName": "self73-firstname",
        "email": "self73@gmail.com"
    },
    {
        "id": 74,
        "username": "self74",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self74-lastname",
        "firstName": "self74-firstname",
        "email": "self74@gmail.com"
    },
    {
        "id": 75,
        "username": "self75",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self75-lastname",
        "firstName": "self75-firstname",
        "email": "self75@gmail.com"
    },
    {
        "id": 76,
        "username": "self76",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self76-lastname",
        "firstName": "self76-firstname",
        "email": "self76@gmail.com"
    },
    {
        "id": 77,
        "username": "self77",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self77-lastname",
        "firstName": "self77-firstname",
        "email": "self77@gmail.com"
    },
    {
        "id": 78,
        "username": "self78",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self78-lastname",
        "firstName": "self78-firstname",
        "email": "self78@gmail.com"
    },
    {
        "id": 79,
        "username": "self79",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self79-lastname",
        "firstName": "self79-firstname",
        "email": "self79@gmail.com"
    },
    {
        "id": 80,
        "username": "self80",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self80-lastname",
        "firstName": "self80-firstname",
        "email": "self80@gmail.com"
    },
    {
        "id": 81,
        "username": "self81",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self81-lastname",
        "firstName": "self81-firstname",
        "email": "self81@gmail.com"
    },
    {
        "id": 82,
        "username": "self82",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self82-lastname",
        "firstName": "self82-firstname",
        "email": "self82@gmail.com"
    },
    {
        "id": 83,
        "username": "self83",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self83-lastname",
        "firstName": "self83-firstname",
        "email": "self83@gmail.com"
    },
    {
        "id": 84,
        "username": "self84",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self84-lastname",
        "firstName": "self84-firstname",
        "email": "self84@gmail.com"
    },
    {
        "id": 85,
        "username": "self85",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self85-lastname",
        "firstName": "self85-firstname",
        "email": "self85@gmail.com"
    },
    {
        "id": 86,
        "username": "self86",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self86-lastname",
        "firstName": "self86-firstname",
        "email": "self86@gmail.com"
    },
    {
        "id": 87,
        "username": "self87",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self87-lastname",
        "firstName": "self87-firstname",
        "email": "self87@gmail.com"
    },
    {
        "id": 88,
        "username": "self88",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self88-lastname",
        "firstName": "self88-firstname",
        "email": "self88@gmail.com"
    },
    {
        "id": 89,
        "username": "self89",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self89-lastname",
        "firstName": "self89-firstname",
        "email": "self89@gmail.com"
    },
    {
        "id": 90,
        "username": "self90",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self90-lastname",
        "firstName": "self90-firstname",
        "email": "self90@gmail.com"
    },
    {
        "id": 91,
        "username": "self91",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self91-lastname",
        "firstName": "self91-firstname",
        "email": "self91@gmail.com"
    },
    {
        "id": 92,
        "username": "self92",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self92-lastname",
        "firstName": "self92-firstname",
        "email": "self92@gmail.com"
    },
    {
        "id": 93,
        "username": "self93",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self93-lastname",
        "firstName": "self93-firstname",
        "email": "self93@gmail.com"
    },
    {
        "id": 94,
        "username": "self94",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self94-lastname",
        "firstName": "self94-firstname",
        "email": "self94@gmail.com"
    },
    {
        "id": 95,
        "username": "self95",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self95-lastname",
        "firstName": "self95-firstname",
        "email": "self95@gmail.com"
    },
    {
        "id": 96,
        "username": "self96",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self96-lastname",
        "firstName": "self96-firstname",
        "email": "self96@gmail.com"
    },
    {
        "id": 97,
        "username": "self97",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self97-lastname",
        "firstName": "self97-firstname",
        "email": "self97@gmail.com"
    },
    {
        "id": 98,
        "username": "self98",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self98-lastname",
        "firstName": "self98-firstname",
        "email": "self98@gmail.com"
    },
    {
        "id": 99,
        "username": "self99",
        "activated": 0,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastName": "self99-lastname",
        "firstName": "self99-firstname",
        "email": "self99@gmail.com"
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
`username` is a search parameter and will match as long as it is contained partially
{% endhint %}

