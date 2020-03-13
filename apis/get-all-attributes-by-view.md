---
description: Get all attributes in view
---

# GET-all-attributes-by-view

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/attributes/view/:viewId" %}
{% api-method-summary %}
Get all attributes in view
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id.
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
[
    {
        "id": 1,
        "name": "string attribute",
        "description": "string attribute description",
        "type": "string"
    },
    {
        "id": 2,
        "name": "text attribute",
        "description": "text attribute description",
        "type": "text"
    },
    {
        "id": 3,
        "name": "number attribute",
        "description": "number attribute description",
        "type": "number",
        "format": "0.0"
    },
    {
        "id": 4,
        "name": "date attribute",
        "description": "date attribute description",
        "type": "date",
        "format": "DD-MM-YYYY"
    },
    {
        "id": 5,
        "name": "currency attribute",
        "description": "currency attribute description",
        "type": "currency",
        "showCurrencyCountry": true
    },
    {
        "id": 6,
        "name": "volume attribute",
        "description": "volume attribute description",
        "type": "volume",
        "format": "0.0"
    },
    {
        "id": 7,
        "name": "dimension attribute",
        "description": "dimension attribute description",
        "type": "dimension",
        "format": "0.0"
    },
    {
        "id": 8,
        "name": "area attribute",
        "description": "area attribute description",
        "type": "area",
        "format": "0.0"
    },
    {
        "id": 9,
        "name": "length attribute",
        "description": "length attribute description",
        "type": "length",
        "format": "0.0"
    },
    {
        "id": 10,
        "name": "width attribute",
        "description": "width attribute description",
        "type": "width",
        "format": "0.0"
    },
    {
        "id": 11,
        "name": "height attribute",
        "description": "height attribute description",
        "type": "height",
        "format": "0.0"
    },
    {
        "id": 12,
        "name": "select attribute",
        "description": "select attribute description",
        "type": "select",
        "pair1": [
            {
                "id": 10,
                "key": "key1",
                "value": "value1"
            },
            {
                "id": 11,
                "key": "key2",
                "value": "value2"
            },
            {
                "id": 12,
                "key": "key3",
                "value": "value3"
            },
            {
                "id": 13,
                "key": "key4",
                "value": "value4"
            },
            {
                "id": 14,
                "key": "key5",
                "value": "value5"
            },
            {
                "id": 15,
                "key": "key6",
                "value": "value6"
            },
            {
                "id": 16,
                "key": "key7",
                "value": "value7"
            },
            {
                "id": 17,
                "key": "key8",
                "value": "value8"
            },
            {
                "id": 18,
                "key": "key9",
                "value": "value9"
            }
        ]
    },
    {
        "id": 13,
        "name": "doubleselect attribute",
        "description": "doubleselect attribute description",
        "type": "doubleselect",
        "pair1": [
            {
                "id": 19,
                "key": "key1",
                "value": "value1"
            },
            {
                "id": 20,
                "key": "key2",
                "value": "value2"
            },
            {
                "id": 21,
                "key": "key3",
                "value": "value3"
            },
            {
                "id": 22,
                "key": "key4",
                "value": "value4"
            },
            {
                "id": 23,
                "key": "key5",
                "value": "value5"
            },
            {
                "id": 24,
                "key": "key6",
                "value": "value6"
            },
            {
                "id": 25,
                "key": "key7",
                "value": "value7"
            },
            {
                "id": 26,
                "key": "key8",
                "value": "value8"
            },
            {
                "id": 27,
                "key": "key9",
                "value": "value9"
            }
        ],
        "pair2": [
            {
                "id": 28,
                "key1": "key1",
                "key2": "xkey11",
                "value": "xvalue11"
            },
            {
                "id": 29,
                "key1": "key1",
                "key2": "xkey12",
                "value": "xvalue12"
            },
            {
                "id": 30,
                "key1": "key1",
                "key2": "xkey13",
                "value": "xvalue13"
            },
            {
                "id": 31,
                "key1": "key1",
                "key2": "xkey14",
                "value": "xvalue14"
            },
            {
                "id": 32,
                "key1": "key1",
                "key2": "xkey15",
                "value": "xvalue15"
            },
            {
                "id": 33,
                "key1": "key1",
                "key2": "xkey16",
                "value": "xvalue16"
            },
            {
                "id": 34,
                "key1": "key1",
                "key2": "xkey17",
                "value": "xvalue17"
            },
            {
                "id": 35,
                "key1": "key1",
                "key2": "xkey18",
                "value": "xvalue18"
            },
            {
                "id": 36,
                "key1": "key1",
                "key2": "xkey19",
                "value": "xvalue19"
            },
            {
                "id": 37,
                "key1": "key2",
                "key2": "xkey21",
                "value": "xvalue21"
            },
            {
                "id": 38,
                "key1": "key2",
                "key2": "xkey22",
                "value": "xvalue22"
            },
            {
                "id": 39,
                "key1": "key2",
                "key2": "xkey23",
                "value": "xvalue23"
            },
            {
                "id": 40,
                "key1": "key2",
                "key2": "xkey24",
                "value": "xvalue24"
            },
            {
                "id": 41,
                "key1": "key2",
                "key2": "xkey25",
                "value": "xvalue25"
            },
            {
                "id": 42,
                "key1": "key2",
                "key2": "xkey26",
                "value": "xvalue26"
            },
            {
                "id": 43,
                "key1": "key2",
                "key2": "xkey27",
                "value": "xvalue27"
            },
            {
                "id": 44,
                "key1": "key2",
                "key2": "xkey28",
                "value": "xvalue28"
            },
            {
                "id": 45,
                "key1": "key2",
                "key2": "xkey29",
                "value": "xvalue29"
            },
            {
                "id": 46,
                "key1": "key3",
                "key2": "xkey31",
                "value": "xvalue31"
            },
            {
                "id": 47,
                "key1": "key3",
                "key2": "xkey32",
                "value": "xvalue32"
            },
            {
                "id": 48,
                "key1": "key3",
                "key2": "xkey33",
                "value": "xvalue33"
            },
            {
                "id": 49,
                "key1": "key3",
                "key2": "xkey34",
                "value": "xvalue34"
            },
            {
                "id": 50,
                "key1": "key3",
                "key2": "xkey35",
                "value": "xvalue35"
            },
            {
                "id": 51,
                "key1": "key3",
                "key2": "xkey36",
                "value": "xvalue36"
            },
            {
                "id": 52,
                "key1": "key3",
                "key2": "xkey37",
                "value": "xvalue37"
            },
            {
                "id": 53,
                "key1": "key3",
                "key2": "xkey38",
                "value": "xvalue38"
            },
            {
                "id": 54,
                "key1": "key3",
                "key2": "xkey39",
                "value": "xvalue39"
            },
            {
                "id": 55,
                "key1": "key4",
                "key2": "xkey41",
                "value": "xvalue41"
            },
            {
                "id": 56,
                "key1": "key4",
                "key2": "xkey42",
                "value": "xvalue42"
            },
            {
                "id": 57,
                "key1": "key4",
                "key2": "xkey43",
                "value": "xvalue43"
            },
            {
                "id": 58,
                "key1": "key4",
                "key2": "xkey44",
                "value": "xvalue44"
            },
            {
                "id": 59,
                "key1": "key4",
                "key2": "xkey45",
                "value": "xvalue45"
            },
            {
                "id": 60,
                "key1": "key4",
                "key2": "xkey46",
                "value": "xvalue46"
            },
            {
                "id": 61,
                "key1": "key4",
                "key2": "xkey47",
                "value": "xvalue47"
            },
            {
                "id": 62,
                "key1": "key4",
                "key2": "xkey48",
                "value": "xvalue48"
            },
            {
                "id": 63,
                "key1": "key4",
                "key2": "xkey49",
                "value": "xvalue49"
            },
            {
                "id": 64,
                "key1": "key5",
                "key2": "xkey51",
                "value": "xvalue51"
            },
            {
                "id": 65,
                "key1": "key5",
                "key2": "xkey52",
                "value": "xvalue52"
            },
            {
                "id": 66,
                "key1": "key5",
                "key2": "xkey53",
                "value": "xvalue53"
            },
            {
                "id": 67,
                "key1": "key5",
                "key2": "xkey54",
                "value": "xvalue54"
            },
            {
                "id": 68,
                "key1": "key5",
                "key2": "xkey55",
                "value": "xvalue55"
            },
            {
                "id": 69,
                "key1": "key5",
                "key2": "xkey56",
                "value": "xvalue56"
            },
            {
                "id": 70,
                "key1": "key5",
                "key2": "xkey57",
                "value": "xvalue57"
            },
            {
                "id": 71,
                "key1": "key5",
                "key2": "xkey58",
                "value": "xvalue58"
            },
            {
                "id": 72,
                "key1": "key5",
                "key2": "xkey59",
                "value": "xvalue59"
            },
            {
                "id": 73,
                "key1": "key6",
                "key2": "xkey61",
                "value": "xvalue61"
            },
            {
                "id": 74,
                "key1": "key6",
                "key2": "xkey62",
                "value": "xvalue62"
            },
            {
                "id": 75,
                "key1": "key6",
                "key2": "xkey63",
                "value": "xvalue63"
            },
            {
                "id": 76,
                "key1": "key6",
                "key2": "xkey64",
                "value": "xvalue64"
            },
            {
                "id": 77,
                "key1": "key6",
                "key2": "xkey65",
                "value": "xvalue65"
            },
            {
                "id": 78,
                "key1": "key6",
                "key2": "xkey66",
                "value": "xvalue66"
            },
            {
                "id": 79,
                "key1": "key6",
                "key2": "xkey67",
                "value": "xvalue67"
            },
            {
                "id": 80,
                "key1": "key6",
                "key2": "xkey68",
                "value": "xvalue68"
            },
            {
                "id": 81,
                "key1": "key6",
                "key2": "xkey69",
                "value": "xvalue69"
            },
            {
                "id": 82,
                "key1": "key7",
                "key2": "xkey71",
                "value": "xvalue71"
            },
            {
                "id": 83,
                "key1": "key7",
                "key2": "xkey72",
                "value": "xvalue72"
            },
            {
                "id": 84,
                "key1": "key7",
                "key2": "xkey73",
                "value": "xvalue73"
            },
            {
                "id": 85,
                "key1": "key7",
                "key2": "xkey74",
                "value": "xvalue74"
            },
            {
                "id": 86,
                "key1": "key7",
                "key2": "xkey75",
                "value": "xvalue75"
            },
            {
                "id": 87,
                "key1": "key7",
                "key2": "xkey76",
                "value": "xvalue76"
            },
            {
                "id": 88,
                "key1": "key7",
                "key2": "xkey77",
                "value": "xvalue77"
            },
            {
                "id": 89,
                "key1": "key7",
                "key2": "xkey78",
                "value": "xvalue78"
            },
            {
                "id": 90,
                "key1": "key7",
                "key2": "xkey79",
                "value": "xvalue79"
            },
            {
                "id": 91,
                "key1": "key8",
                "key2": "xkey81",
                "value": "xvalue81"
            },
            {
                "id": 92,
                "key1": "key8",
                "key2": "xkey82",
                "value": "xvalue82"
            },
            {
                "id": 93,
                "key1": "key8",
                "key2": "xkey83",
                "value": "xvalue83"
            },
            {
                "id": 94,
                "key1": "key8",
                "key2": "xkey84",
                "value": "xvalue84"
            },
            {
                "id": 95,
                "key1": "key8",
                "key2": "xkey85",
                "value": "xvalue85"
            },
            {
                "id": 96,
                "key1": "key8",
                "key2": "xkey86",
                "value": "xvalue86"
            },
            {
                "id": 97,
                "key1": "key8",
                "key2": "xkey87",
                "value": "xvalue87"
            },
            {
                "id": 98,
                "key1": "key8",
                "key2": "xkey88",
                "value": "xvalue88"
            },
            {
                "id": 99,
                "key1": "key8",
                "key2": "xkey89",
                "value": "xvalue89"
            },
            {
                "id": 100,
                "key1": "key9",
                "key2": "xkey91",
                "value": "xvalue91"
            },
            {
                "id": 101,
                "key1": "key9",
                "key2": "xkey92",
                "value": "xvalue92"
            },
            {
                "id": 102,
                "key1": "key9",
                "key2": "xkey93",
                "value": "xvalue93"
            },
            {
                "id": 103,
                "key1": "key9",
                "key2": "xkey94",
                "value": "xvalue94"
            },
            {
                "id": 104,
                "key1": "key9",
                "key2": "xkey95",
                "value": "xvalue95"
            },
            {
                "id": 105,
                "key1": "key9",
                "key2": "xkey96",
                "value": "xvalue96"
            },
            {
                "id": 106,
                "key1": "key9",
                "key2": "xkey97",
                "value": "xvalue97"
            },
            {
                "id": 107,
                "key1": "key9",
                "key2": "xkey98",
                "value": "xvalue98"
            },
            {
                "id": 108,
                "key1": "key9",
                "key2": "xkey99",
                "value": "xvalue99"
            }
        ]
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



