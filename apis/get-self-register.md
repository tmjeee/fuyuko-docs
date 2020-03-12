---
description: Get self registration
---

# GET-self-register

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/self-registers" %}
{% api-method-summary %}
Get self registrations
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication tokens.
{% endapi-method-parameter %}
{% endapi-method-headers %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
[
    {
        "id": 2,
        "username": "self2",
        "email": "self2@gmail.com",
        "firstName": "self2-firstname",
        "lastName": "self2-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 3,
        "username": "self3",
        "email": "self3@gmail.com",
        "firstName": "self3-firstname",
        "lastName": "self3-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 4,
        "username": "self4",
        "email": "self4@gmail.com",
        "firstName": "self4-firstname",
        "lastName": "self4-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 5,
        "username": "self5",
        "email": "self5@gmail.com",
        "firstName": "self5-firstname",
        "lastName": "self5-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 6,
        "username": "self6",
        "email": "self6@gmail.com",
        "firstName": "self6-firstname",
        "lastName": "self6-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 7,
        "username": "self7",
        "email": "self7@gmail.com",
        "firstName": "self7-firstname",
        "lastName": "self7-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 8,
        "username": "self8",
        "email": "self8@gmail.com",
        "firstName": "self8-firstname",
        "lastName": "self8-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 9,
        "username": "self9",
        "email": "self9@gmail.com",
        "firstName": "self9-firstname",
        "lastName": "self9-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 10,
        "username": "self10",
        "email": "self10@gmail.com",
        "firstName": "self10-firstname",
        "lastName": "self10-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 11,
        "username": "self11",
        "email": "self11@gmail.com",
        "firstName": "self11-firstname",
        "lastName": "self11-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 12,
        "username": "self12",
        "email": "self12@gmail.com",
        "firstName": "self12-firstname",
        "lastName": "self12-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 13,
        "username": "self13",
        "email": "self13@gmail.com",
        "firstName": "self13-firstname",
        "lastName": "self13-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 14,
        "username": "self14",
        "email": "self14@gmail.com",
        "firstName": "self14-firstname",
        "lastName": "self14-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 15,
        "username": "self15",
        "email": "self15@gmail.com",
        "firstName": "self15-firstname",
        "lastName": "self15-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 16,
        "username": "self16",
        "email": "self16@gmail.com",
        "firstName": "self16-firstname",
        "lastName": "self16-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 17,
        "username": "self17",
        "email": "self17@gmail.com",
        "firstName": "self17-firstname",
        "lastName": "self17-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 18,
        "username": "self18",
        "email": "self18@gmail.com",
        "firstName": "self18-firstname",
        "lastName": "self18-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 19,
        "username": "self19",
        "email": "self19@gmail.com",
        "firstName": "self19-firstname",
        "lastName": "self19-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 20,
        "username": "self20",
        "email": "self20@gmail.com",
        "firstName": "self20-firstname",
        "lastName": "self20-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 21,
        "username": "self21",
        "email": "self21@gmail.com",
        "firstName": "self21-firstname",
        "lastName": "self21-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 22,
        "username": "self22",
        "email": "self22@gmail.com",
        "firstName": "self22-firstname",
        "lastName": "self22-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 23,
        "username": "self23",
        "email": "self23@gmail.com",
        "firstName": "self23-firstname",
        "lastName": "self23-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 24,
        "username": "self24",
        "email": "self24@gmail.com",
        "firstName": "self24-firstname",
        "lastName": "self24-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 25,
        "username": "self25",
        "email": "self25@gmail.com",
        "firstName": "self25-firstname",
        "lastName": "self25-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 26,
        "username": "self26",
        "email": "self26@gmail.com",
        "firstName": "self26-firstname",
        "lastName": "self26-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 27,
        "username": "self27",
        "email": "self27@gmail.com",
        "firstName": "self27-firstname",
        "lastName": "self27-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 28,
        "username": "self28",
        "email": "self28@gmail.com",
        "firstName": "self28-firstname",
        "lastName": "self28-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 29,
        "username": "self29",
        "email": "self29@gmail.com",
        "firstName": "self29-firstname",
        "lastName": "self29-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 30,
        "username": "self30",
        "email": "self30@gmail.com",
        "firstName": "self30-firstname",
        "lastName": "self30-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 31,
        "username": "self31",
        "email": "self31@gmail.com",
        "firstName": "self31-firstname",
        "lastName": "self31-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 32,
        "username": "self32",
        "email": "self32@gmail.com",
        "firstName": "self32-firstname",
        "lastName": "self32-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 33,
        "username": "self33",
        "email": "self33@gmail.com",
        "firstName": "self33-firstname",
        "lastName": "self33-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 34,
        "username": "self34",
        "email": "self34@gmail.com",
        "firstName": "self34-firstname",
        "lastName": "self34-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 35,
        "username": "self35",
        "email": "self35@gmail.com",
        "firstName": "self35-firstname",
        "lastName": "self35-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 36,
        "username": "self36",
        "email": "self36@gmail.com",
        "firstName": "self36-firstname",
        "lastName": "self36-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 37,
        "username": "self37",
        "email": "self37@gmail.com",
        "firstName": "self37-firstname",
        "lastName": "self37-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 38,
        "username": "self38",
        "email": "self38@gmail.com",
        "firstName": "self38-firstname",
        "lastName": "self38-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 39,
        "username": "self39",
        "email": "self39@gmail.com",
        "firstName": "self39-firstname",
        "lastName": "self39-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 40,
        "username": "self40",
        "email": "self40@gmail.com",
        "firstName": "self40-firstname",
        "lastName": "self40-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 41,
        "username": "self41",
        "email": "self41@gmail.com",
        "firstName": "self41-firstname",
        "lastName": "self41-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 42,
        "username": "self42",
        "email": "self42@gmail.com",
        "firstName": "self42-firstname",
        "lastName": "self42-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 43,
        "username": "self43",
        "email": "self43@gmail.com",
        "firstName": "self43-firstname",
        "lastName": "self43-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 44,
        "username": "self44",
        "email": "self44@gmail.com",
        "firstName": "self44-firstname",
        "lastName": "self44-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 45,
        "username": "self45",
        "email": "self45@gmail.com",
        "firstName": "self45-firstname",
        "lastName": "self45-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 46,
        "username": "self46",
        "email": "self46@gmail.com",
        "firstName": "self46-firstname",
        "lastName": "self46-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 47,
        "username": "self47",
        "email": "self47@gmail.com",
        "firstName": "self47-firstname",
        "lastName": "self47-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 48,
        "username": "self48",
        "email": "self48@gmail.com",
        "firstName": "self48-firstname",
        "lastName": "self48-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 49,
        "username": "self49",
        "email": "self49@gmail.com",
        "firstName": "self49-firstname",
        "lastName": "self49-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 50,
        "username": "self50",
        "email": "self50@gmail.com",
        "firstName": "self50-firstname",
        "lastName": "self50-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 51,
        "username": "self51",
        "email": "self51@gmail.com",
        "firstName": "self51-firstname",
        "lastName": "self51-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 52,
        "username": "self52",
        "email": "self52@gmail.com",
        "firstName": "self52-firstname",
        "lastName": "self52-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 53,
        "username": "self53",
        "email": "self53@gmail.com",
        "firstName": "self53-firstname",
        "lastName": "self53-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 54,
        "username": "self54",
        "email": "self54@gmail.com",
        "firstName": "self54-firstname",
        "lastName": "self54-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 55,
        "username": "self55",
        "email": "self55@gmail.com",
        "firstName": "self55-firstname",
        "lastName": "self55-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 56,
        "username": "self56",
        "email": "self56@gmail.com",
        "firstName": "self56-firstname",
        "lastName": "self56-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 57,
        "username": "self57",
        "email": "self57@gmail.com",
        "firstName": "self57-firstname",
        "lastName": "self57-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 58,
        "username": "self58",
        "email": "self58@gmail.com",
        "firstName": "self58-firstname",
        "lastName": "self58-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 59,
        "username": "self59",
        "email": "self59@gmail.com",
        "firstName": "self59-firstname",
        "lastName": "self59-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 60,
        "username": "self60",
        "email": "self60@gmail.com",
        "firstName": "self60-firstname",
        "lastName": "self60-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 61,
        "username": "self61",
        "email": "self61@gmail.com",
        "firstName": "self61-firstname",
        "lastName": "self61-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 62,
        "username": "self62",
        "email": "self62@gmail.com",
        "firstName": "self62-firstname",
        "lastName": "self62-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 63,
        "username": "self63",
        "email": "self63@gmail.com",
        "firstName": "self63-firstname",
        "lastName": "self63-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 64,
        "username": "self64",
        "email": "self64@gmail.com",
        "firstName": "self64-firstname",
        "lastName": "self64-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 65,
        "username": "self65",
        "email": "self65@gmail.com",
        "firstName": "self65-firstname",
        "lastName": "self65-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 66,
        "username": "self66",
        "email": "self66@gmail.com",
        "firstName": "self66-firstname",
        "lastName": "self66-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 67,
        "username": "self67",
        "email": "self67@gmail.com",
        "firstName": "self67-firstname",
        "lastName": "self67-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 68,
        "username": "self68",
        "email": "self68@gmail.com",
        "firstName": "self68-firstname",
        "lastName": "self68-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 69,
        "username": "self69",
        "email": "self69@gmail.com",
        "firstName": "self69-firstname",
        "lastName": "self69-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 70,
        "username": "self70",
        "email": "self70@gmail.com",
        "firstName": "self70-firstname",
        "lastName": "self70-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 71,
        "username": "self71",
        "email": "self71@gmail.com",
        "firstName": "self71-firstname",
        "lastName": "self71-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 72,
        "username": "self72",
        "email": "self72@gmail.com",
        "firstName": "self72-firstname",
        "lastName": "self72-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 73,
        "username": "self73",
        "email": "self73@gmail.com",
        "firstName": "self73-firstname",
        "lastName": "self73-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 74,
        "username": "self74",
        "email": "self74@gmail.com",
        "firstName": "self74-firstname",
        "lastName": "self74-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 75,
        "username": "self75",
        "email": "self75@gmail.com",
        "firstName": "self75-firstname",
        "lastName": "self75-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 76,
        "username": "self76",
        "email": "self76@gmail.com",
        "firstName": "self76-firstname",
        "lastName": "self76-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 77,
        "username": "self77",
        "email": "self77@gmail.com",
        "firstName": "self77-firstname",
        "lastName": "self77-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 78,
        "username": "self78",
        "email": "self78@gmail.com",
        "firstName": "self78-firstname",
        "lastName": "self78-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 79,
        "username": "self79",
        "email": "self79@gmail.com",
        "firstName": "self79-firstname",
        "lastName": "self79-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 80,
        "username": "self80",
        "email": "self80@gmail.com",
        "firstName": "self80-firstname",
        "lastName": "self80-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 81,
        "username": "self81",
        "email": "self81@gmail.com",
        "firstName": "self81-firstname",
        "lastName": "self81-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 82,
        "username": "self82",
        "email": "self82@gmail.com",
        "firstName": "self82-firstname",
        "lastName": "self82-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 83,
        "username": "self83",
        "email": "self83@gmail.com",
        "firstName": "self83-firstname",
        "lastName": "self83-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 84,
        "username": "self84",
        "email": "self84@gmail.com",
        "firstName": "self84-firstname",
        "lastName": "self84-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 85,
        "username": "self85",
        "email": "self85@gmail.com",
        "firstName": "self85-firstname",
        "lastName": "self85-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 86,
        "username": "self86",
        "email": "self86@gmail.com",
        "firstName": "self86-firstname",
        "lastName": "self86-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 87,
        "username": "self87",
        "email": "self87@gmail.com",
        "firstName": "self87-firstname",
        "lastName": "self87-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 88,
        "username": "self88",
        "email": "self88@gmail.com",
        "firstName": "self88-firstname",
        "lastName": "self88-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 89,
        "username": "self89",
        "email": "self89@gmail.com",
        "firstName": "self89-firstname",
        "lastName": "self89-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 90,
        "username": "self90",
        "email": "self90@gmail.com",
        "firstName": "self90-firstname",
        "lastName": "self90-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 91,
        "username": "self91",
        "email": "self91@gmail.com",
        "firstName": "self91-firstname",
        "lastName": "self91-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 92,
        "username": "self92",
        "email": "self92@gmail.com",
        "firstName": "self92-firstname",
        "lastName": "self92-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 93,
        "username": "self93",
        "email": "self93@gmail.com",
        "firstName": "self93-firstname",
        "lastName": "self93-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 94,
        "username": "self94",
        "email": "self94@gmail.com",
        "firstName": "self94-firstname",
        "lastName": "self94-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 95,
        "username": "self95",
        "email": "self95@gmail.com",
        "firstName": "self95-firstname",
        "lastName": "self95-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 96,
        "username": "self96",
        "email": "self96@gmail.com",
        "firstName": "self96-firstname",
        "lastName": "self96-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 97,
        "username": "self97",
        "email": "self97@gmail.com",
        "firstName": "self97-firstname",
        "lastName": "self97-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 98,
        "username": "self98",
        "email": "self98@gmail.com",
        "firstName": "self98-firstname",
        "lastName": "self98-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 99,
        "username": "self99",
        "email": "self99@gmail.com",
        "firstName": "self99-firstname",
        "lastName": "self99-lastname",
        "creationDate": "2020-03-09T23:04:14.000Z",
        "activated": 0
    },
    {
        "id": 100,
        "username": "ccccctest1",
        "email": "ccccctest1@gmail.com",
        "firstName": "ccccctest1",
        "lastName": "ccccctest1",
        "creationDate": "2020-03-12T05:49:32.000Z",
        "activated": 0
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



