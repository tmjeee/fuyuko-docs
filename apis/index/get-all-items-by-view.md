---
description: Get all items in a view
---

# GET-all-items-by-view

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/items" %}
{% api-method-summary %}
Get all items in a view
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

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="number" required=false %}
limit for pagination, greater than 0
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="number" required=false %}
offset for pagination, 0 or greater
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
  "limit": 10,
  "offset": 0,
  "total": 200,
  "payload": [
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 6832"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 46581"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 10061
            }
        },
        "4": {
            "attributeId": 4,
            "val": {
                "type": "date",
                "value": "12-10-1988"
            }
        },
        "5": {
            "attributeId": 5,
            "val": {
                "type": "currency",
                "value": 36189.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 42166,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 46549,
                "width": 55063,
                "height": 43385,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 67765,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 56534,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 62043,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 28075,
                "unit": "cm"
            }
        },
        "12": {
            "attributeId": 12,
            "val": {
                "type": "select",
                "key": "key2"
            }
        },
        "13": {
            "attributeId": 13,
            "val": {
                "type": "doubleselect",
                "key1": "key3",
                "key2": "xkey35"
            }
        },
        "id": 1,
        "parentId": null,
        "images": [
            {
                "id": 1,
                "name": "0007.jpg",
                "size": 223083
            },
            {
                "id": 2,
                "name": "0008.jpg",
                "size": 37514
            },
            {
                "id": 3,
                "name": "0009.jpg",
                "size": 85183
            }
        ],
        "description": "Item-1 Description",
        "name": "Item-1",
        "children": [
            {
                "1": {
                    "attributeId": 1,
                    "val": {
                        "type": "string",
                        "value": "some string 99684"
                    }
                },
                "2": {
                    "attributeId": 2,
                    "val": {
                        "type": "text",
                        "value": "some text 49867"
                    }
                },
                "3": {
                    "attributeId": 3,
                    "val": {
                        "type": "number",
                        "value": 91159
                    }
                },
                "4": {
                    "attributeId": 4,
                    "val": {
                        "type": "date",
                        "value": "12-10-1988"
                    }
                },
                "5": {
                    "attributeId": 5,
                    "val": {
                        "type": "currency",
                        "value": 73558.1,
                        "country": "AUD"
                    }
                },
                "6": {
                    "attributeId": 6,
                    "val": {
                        "type": "volume",
                        "value": 82449,
                        "unit": "l"
                    }
                },
                "7": {
                    "attributeId": 7,
                    "val": {
                        "type": "dimension",
                        "length": 89736,
                        "width": 80450,
                        "height": 2344,
                        "unit": "cm"
                    }
                },
                "8": {
                    "attributeId": 8,
                    "val": {
                        "type": "area",
                        "value": 59993,
                        "unit": "cm"
                    }
                },
                "9": {
                    "attributeId": 9,
                    "val": {
                        "type": "length",
                        "value": 47115,
                        "unit": "cm"
                    }
                },
                "10": {
                    "attributeId": 10,
                    "val": {
                        "type": "width",
                        "value": 45111,
                        "unit": "cm"
                    }
                },
                "11": {
                    "attributeId": 11,
                    "val": {
                        "type": "height",
                        "value": 78495,
                        "unit": "cm"
                    }
                },
                "12": {
                    "attributeId": 12,
                    "val": {
                        "type": "select",
                        "key": "key2"
                    }
                },
                "13": {
                    "attributeId": 13,
                    "val": {
                        "type": "doubleselect",
                        "key1": "key3",
                        "key2": "xkey35"
                    }
                },
                "id": 2,
                "parentId": 1,
                "images": [
                    {
                        "id": 4,
                        "name": "0001.jpg",
                        "size": 57466
                    },
                    {
                        "id": 5,
                        "name": "0002.jpg",
                        "size": 124300
                    },
                    {
                        "id": 6,
                        "name": "0003.jpg",
                        "size": 83256
                    }
                ],
                "description": "Item-1-1 Description",
                "name": "Item-1-1",
                "children": []
            },
            {
                "1": {
                    "attributeId": 1,
                    "val": {
                        "type": "string",
                        "value": "some string 45279"
                    }
                },
                "2": {
                    "attributeId": 2,
                    "val": {
                        "type": "text",
                        "value": "some text 5756"
                    }
                },
                "3": {
                    "attributeId": 3,
                    "val": {
                        "type": "number",
                        "value": 84056
                    }
                },
                "4": {
                    "attributeId": 4,
                    "val": {
                        "type": "date",
                        "value": "12-10-1988"
                    }
                },
                "5": {
                    "attributeId": 5,
                    "val": {
                        "type": "currency",
                        "value": 15006.1,
                        "country": "AUD"
                    }
                },
                "6": {
                    "attributeId": 6,
                    "val": {
                        "type": "volume",
                        "value": 23563,
                        "unit": "l"
                    }
                },
                "7": {
                    "attributeId": 7,
                    "val": {
                        "type": "dimension",
                        "length": 10059,
                        "width": 68722,
                        "height": 79232,
                        "unit": "cm"
                    }
                },
                "8": {
                    "attributeId": 8,
                    "val": {
                        "type": "area",
                        "value": 72905,
                        "unit": "cm"
                    }
                },
                "9": {
                    "attributeId": 9,
                    "val": {
                        "type": "length",
                        "value": 87435,
                        "unit": "cm"
                    }
                },
                "10": {
                    "attributeId": 10,
                    "val": {
                        "type": "width",
                        "value": 65800,
                        "unit": "cm"
                    }
                },
                "11": {
                    "attributeId": 11,
                    "val": {
                        "type": "height",
                        "value": 36754,
                        "unit": "cm"
                    }
                },
                "12": {
                    "attributeId": 12,
                    "val": {
                        "type": "select",
                        "key": "key2"
                    }
                },
                "13": {
                    "attributeId": 13,
                    "val": {
                        "type": "doubleselect",
                        "key1": "key3",
                        "key2": "xkey35"
                    }
                },
                "id": 3,
                "parentId": 1,
                "images": [
                    {
                        "id": 7,
                        "name": "0004.jpg",
                        "size": 75170
                    },
                    {
                        "id": 8,
                        "name": "0005.jpg",
                        "size": 26242
                    },
                    {
                        "id": 9,
                        "name": "0006.jpg",
                        "size": 38305
                    }
                ],
                "description": "Item-1-2 Description",
                "name": "Item-1-2",
                "children": []
            }
        ]
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 27725"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 21912"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 85954
            }
        },
        "4": {
            "attributeId": 4,
            "val": {
                "type": "date",
                "value": "12-10-1988"
            }
        },
        "5": {
            "attributeId": 5,
            "val": {
                "type": "currency",
                "value": 74719.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 45511,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 83769,
                "width": 53862,
                "height": 54091,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 4123,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 20082,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 20697,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 95293,
                "unit": "cm"
            }
        },
        "12": {
            "attributeId": 12,
            "val": {
                "type": "select",
                "key": "key2"
            }
        },
        "13": {
            "attributeId": 13,
            "val": {
                "type": "doubleselect",
                "key1": "key3",
                "key2": "xkey35"
            }
        },
        "id": 4,
        "parentId": null,
        "images": [
            {
                "id": 10,
                "name": "0010.jpg",
                "size": 23016
            },
            {
                "id": 11,
                "name": "0011.jpg",
                "size": 115737
            },
            {
                "id": 12,
                "name": "0012.jpg",
                "size": 15793
            }
        ],
        "description": "Item-2 Description",
        "name": "Item-2",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 7579"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 13189"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 23679
            }
        },
        "4": {
            "attributeId": 4,
            "val": {
                "type": "date",
                "value": "12-10-1988"
            }
        },
        "5": {
            "attributeId": 5,
            "val": {
                "type": "currency",
                "value": 71991.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 1806,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 85643,
                "width": 74461,
                "height": 82095,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 93746,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 12482,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 89574,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 19891,
                "unit": "cm"
            }
        },
        "12": {
            "attributeId": 12,
            "val": {
                "type": "select",
                "key": "key2"
            }
        },
        "13": {
            "attributeId": 13,
            "val": {
                "type": "doubleselect",
                "key1": "key3",
                "key2": "xkey35"
            }
        },
        "id": 5,
        "parentId": null,
        "images": [
            {
                "id": 13,
                "name": "0013.jpg",
                "size": 392173
            },
            {
                "id": 14,
                "name": "0014.jpg",
                "size": 35669
            },
            {
                "id": 15,
                "name": "0015.jpg",
                "size": 47898
            }
        ],
        "description": "Item-3 Description",
        "name": "Item-3",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 51926"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 26099"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 95086
            }
        },
        "4": {
            "attributeId": 4,
            "val": {
                "type": "date",
                "value": "12-10-1988"
            }
        },
        "5": {
            "attributeId": 5,
            "val": {
                "type": "currency",
                "value": 79308.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 84452,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 54241,
                "width": 77488,
                "height": 72131,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 95391,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 45675,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 18811,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 76983,
                "unit": "cm"
            }
        },
        "12": {
            "attributeId": 12,
            "val": {
                "type": "select",
                "key": "key2"
            }
        },
        "13": {
            "attributeId": 13,
            "val": {
                "type": "doubleselect",
                "key1": "key3",
                "key2": "xkey35"
            }
        },
        "id": 6,
        "parentId": null,
        "images": [
            {
                "id": 16,
                "name": "0016.jpg",
                "size": 177509
            },
            {
                "id": 17,
                "name": "0017.jpg",
                "size": 281236
            },
            {
                "id": 18,
                "name": "0018.jpg",
                "size": 95705
            }
        ],
        "description": "Item-4 Description",
        "name": "Item-4",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 67288"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 72480"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 90914
            }
        },
        "4": {
            "attributeId": 4,
            "val": {
                "type": "date",
                "value": "12-10-1988"
            }
        },
        "5": {
            "attributeId": 5,
            "val": {
                "type": "currency",
                "value": 84314.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 7691,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 16870,
                "width": 31347,
                "height": 4304,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 23053,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 42357,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 42496,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 38864,
                "unit": "cm"
            }
        },
        "12": {
            "attributeId": 12,
            "val": {
                "type": "select",
                "key": "key2"
            }
        },
        "13": {
            "attributeId": 13,
            "val": {
                "type": "doubleselect",
                "key1": "key3",
                "key2": "xkey35"
            }
        },
        "id": 7,
        "parentId": null,
        "images": [
            {
                "id": 19,
                "name": "0019.jpg",
                "size": 10438
            },
            {
                "id": 20,
                "name": "0020.jpg",
                "size": 17796
            },
            {
                "id": 21,
                "name": "0021.jpg",
                "size": 22667
            }
        ],
        "description": "Item-5 Description",
        "name": "Item-5",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 70827"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 21693"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 22831
            }
        },
        "4": {
            "attributeId": 4,
            "val": {
                "type": "date",
                "value": "12-10-1988"
            }
        },
        "5": {
            "attributeId": 5,
            "val": {
                "type": "currency",
                "value": 46462.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 2916,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 90081,
                "width": 59478,
                "height": 74691,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 1288,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 77397,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 89390,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 96208,
                "unit": "cm"
            }
        },
        "12": {
            "attributeId": 12,
            "val": {
                "type": "select",
                "key": "key2"
            }
        },
        "13": {
            "attributeId": 13,
            "val": {
                "type": "doubleselect",
                "key1": "key3",
                "key2": "xkey35"
            }
        },
        "id": 8,
        "parentId": null,
        "images": [
            {
                "id": 22,
                "name": "0022.jpg",
                "size": 257902
            },
            {
                "id": 23,
                "name": "0023.jpg",
                "size": 37701
            },
            {
                "id": 24,
                "name": "0024.jpg",
                "size": 81916
            }
        ],
        "description": "Item-6 Description",
        "name": "Item-6",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 53958"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 46396"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 42031
            }
        },
        "4": {
            "attributeId": 4,
            "val": {
                "type": "date",
                "value": "12-10-1988"
            }
        },
        "5": {
            "attributeId": 5,
            "val": {
                "type": "currency",
                "value": 54488.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 71274,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 39946,
                "width": 94574,
                "height": 221,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 41459,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 38905,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 38046,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 99546,
                "unit": "cm"
            }
        },
        "12": {
            "attributeId": 12,
            "val": {
                "type": "select",
                "key": "key2"
            }
        },
        "13": {
            "attributeId": 13,
            "val": {
                "type": "doubleselect",
                "key1": "key3",
                "key2": "xkey35"
            }
        },
        "id": 9,
        "parentId": null,
        "images": [
            {
                "id": 25,
                "name": "0025.jpg",
                "size": 29061
            },
            {
                "id": 26,
                "name": "0026.jpg",
                "size": 761031
            },
            {
                "id": 27,
                "name": "0027.jpg",
                "size": 33368
            }
        ],
        "description": "Item-7 Description",
        "name": "Item-7",
        "children": []
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Pagination query parameters `limit` and `offset` must both exists for pagination to work, else the whole set will be returned.
{% endhint %}

