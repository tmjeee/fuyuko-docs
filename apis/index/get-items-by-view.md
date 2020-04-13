---
description: Get items by view
---

# GET-items-by-view

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/items/:itemIds" %}
{% api-method-summary %}
Get items by view
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="itemIds" type="number" required=false %}
Item Ids \(comman separated if many\)
{% endapi-method-parameter %}

{% api-method-parameter name="viewId" type="number" %}
View Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-query-parameters %}
{% api-method-parameter name="limit" type="number" required=false %}
Limit for pagination, greater than 0
{% endapi-method-parameter %}

{% api-method-parameter name="offset" type="number" required=false %}
Offset for pagination, 0 or greater
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
  "payload": [
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 154"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 25027"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 64467
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
                "value": 18500.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 82588,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 48491,
                "width": 71801,
                "height": 79022,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 54658,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 28902,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 18262,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 2737,
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
                "id": 2,
                "name": "0008.jpg",
                "size": 37514,
                "primary": 0
            },
            {
                "id": 3,
                "name": "0009.jpg",
                "size": 85183,
                "primary": 0
            },
            {
                "id": 28,
                "name": "pizza.jpeg",
                "size": 12321,
                "primary": 1
            }
        ],
        "description": "Item-1 Description",
        "name": "Item-1",
        "creationDate": "2020-03-23T06:51:24.000Z",
        "lastUpdate": "2020-03-23T06:51:24.000Z",
        "children": [
            {
                "1": {
                    "attributeId": 1,
                    "val": {
                        "type": "string",
                        "value": "some string 74617"
                    }
                },
                "2": {
                    "attributeId": 2,
                    "val": {
                        "type": "text",
                        "value": "some text 17139"
                    }
                },
                "3": {
                    "attributeId": 3,
                    "val": {
                        "type": "number",
                        "value": 70498
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
                        "value": 13247.1,
                        "country": "AUD"
                    }
                },
                "6": {
                    "attributeId": 6,
                    "val": {
                        "type": "volume",
                        "value": 92411,
                        "unit": "l"
                    }
                },
                "7": {
                    "attributeId": 7,
                    "val": {
                        "type": "dimension",
                        "length": 20923,
                        "width": 18775,
                        "height": 13,
                        "unit": "cm"
                    }
                },
                "8": {
                    "attributeId": 8,
                    "val": {
                        "type": "area",
                        "value": 4459,
                        "unit": "cm"
                    }
                },
                "9": {
                    "attributeId": 9,
                    "val": {
                        "type": "length",
                        "value": 28278,
                        "unit": "cm"
                    }
                },
                "10": {
                    "attributeId": 10,
                    "val": {
                        "type": "width",
                        "value": 96118,
                        "unit": "cm"
                    }
                },
                "11": {
                    "attributeId": 11,
                    "val": {
                        "type": "height",
                        "value": 48972,
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
                        "size": 57466,
                        "primary": 1
                    },
                    {
                        "id": 5,
                        "name": "0002.jpg",
                        "size": 124300,
                        "primary": 0
                    },
                    {
                        "id": 6,
                        "name": "0003.jpg",
                        "size": 83256,
                        "primary": 0
                    }
                ],
                "description": "Item-1-1 Description",
                "name": "Item-1-1",
                "creationDate": "2020-03-23T06:51:24.000Z",
                "lastUpdate": "2020-03-23T06:51:24.000Z",
                "children": []
            },
            {
                "1": {
                    "attributeId": 1,
                    "val": {
                        "type": "string",
                        "value": "some string 23228"
                    }
                },
                "2": {
                    "attributeId": 2,
                    "val": {
                        "type": "text",
                        "value": "some text 47665"
                    }
                },
                "3": {
                    "attributeId": 3,
                    "val": {
                        "type": "number",
                        "value": 1654
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
                        "value": 45397.1,
                        "country": "AUD"
                    }
                },
                "6": {
                    "attributeId": 6,
                    "val": {
                        "type": "volume",
                        "value": 43900,
                        "unit": "l"
                    }
                },
                "7": {
                    "attributeId": 7,
                    "val": {
                        "type": "dimension",
                        "length": 57836,
                        "width": 48821,
                        "height": 39858,
                        "unit": "cm"
                    }
                },
                "8": {
                    "attributeId": 8,
                    "val": {
                        "type": "area",
                        "value": 83806,
                        "unit": "cm"
                    }
                },
                "9": {
                    "attributeId": 9,
                    "val": {
                        "type": "length",
                        "value": 2217,
                        "unit": "cm"
                    }
                },
                "10": {
                    "attributeId": 10,
                    "val": {
                        "type": "width",
                        "value": 83410,
                        "unit": "cm"
                    }
                },
                "11": {
                    "attributeId": 11,
                    "val": {
                        "type": "height",
                        "value": 40894,
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
                        "size": 75170,
                        "primary": 1
                    },
                    {
                        "id": 8,
                        "name": "0005.jpg",
                        "size": 26242,
                        "primary": 0
                    },
                    {
                        "id": 9,
                        "name": "0006.jpg",
                        "size": 38305,
                        "primary": 0
                    }
                ],
                "description": "Item-1-2 Description",
                "name": "Item-1-2",
                "creationDate": "2020-03-23T06:51:25.000Z",
                "lastUpdate": "2020-03-23T06:51:25.000Z",
                "children": []
            }
        ]
    }
  ]
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
`itemIds` can be comma separated if needs be
{% endhint %}

{% hint style="info" %}
Query parameters limit and offset must both be present in order for pagination to work.
{% endhint %}

