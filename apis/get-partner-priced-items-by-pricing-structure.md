---
description: Get partner priced items by pricing structure
---

# GET-partner-priced-items-by-pricing-structure

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/pricingStructure/:pricingStructureId/pricedItems" %}
{% api-method-summary %}
Get partner priced items by pricing structure
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="pricingStructureId" type="number" required=true %}
Pricing structure Id
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
        "name": "Item-1",
        "description": "Item-1 Description",
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
        "country": "AUD",
        "price": 1.1,
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
                "name": "Item-1-1",
                "description": "Item-1-1 Description",
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
                "country": "AUD",
                "price": 10.1,
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
                "name": "Item-1-2",
                "description": "Item-1-2 Description",
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
                "country": "AUD",
                "price": 10.1,
                "creationDate": "2020-03-23T06:51:25.000Z",
                "lastUpdate": "2020-03-23T06:51:25.000Z",
                "children": []
            }
        ]
    },
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
        "name": "Item-1-1",
        "description": "Item-1-1 Description",
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
        "country": "AUD",
        "price": 10.1,
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
        "name": "Item-1-2",
        "description": "Item-1-2 Description",
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
        "country": "AUD",
        "price": 10.1,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastUpdate": "2020-03-23T06:51:25.000Z",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 18598"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 28828"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 77797
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
                "value": 6862.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 9012,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 54535,
                "width": 27132,
                "height": 8818,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 2624,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 25923,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 82676,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 81882,
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
        "name": "Item-2",
        "description": "Item-2 Description",
        "parentId": null,
        "images": [
            {
                "id": 10,
                "name": "0010.jpg",
                "size": 23016,
                "primary": 0
            },
            {
                "id": 11,
                "name": "0011.jpg",
                "size": 115737,
                "primary": 0
            },
            {
                "id": 12,
                "name": "0012.jpg",
                "size": 15793,
                "primary": 1
            }
        ],
        "country": "AUD",
        "price": 2.2,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastUpdate": "2020-03-23T06:51:25.000Z",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 85614"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 30460"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 63664
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
                "value": 87142.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 56876,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 40800,
                "width": 13810,
                "height": 40028,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 6041,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 94679,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 40524,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 68985,
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
        "name": "Item-3",
        "description": "Item-3 Description",
        "parentId": null,
        "images": [
            {
                "id": 13,
                "name": "0013.jpg",
                "size": 392173,
                "primary": 1
            },
            {
                "id": 14,
                "name": "0014.jpg",
                "size": 35669,
                "primary": 0
            },
            {
                "id": 15,
                "name": "0015.jpg",
                "size": 47898,
                "primary": 0
            }
        ],
        "country": "AUD",
        "price": 3.3,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastUpdate": "2020-03-23T06:51:25.000Z",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 45119"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 38135"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 26281
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
                "value": 46279.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 13008,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 93156,
                "width": 26176,
                "height": 87939,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 59417,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 54836,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 92734,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 14918,
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
        "name": "Item-4",
        "description": "Item-4 Description",
        "parentId": null,
        "images": [
            {
                "id": 16,
                "name": "0016.jpg",
                "size": 177509,
                "primary": 1
            },
            {
                "id": 17,
                "name": "0017.jpg",
                "size": 281236,
                "primary": 0
            },
            {
                "id": 18,
                "name": "0018.jpg",
                "size": 95705,
                "primary": 0
            }
        ],
        "country": "AUD",
        "price": 4.4,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastUpdate": "2020-03-23T06:51:25.000Z",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 12687"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 21223"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 61292
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
                "value": 13402.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 91777,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 36938,
                "width": 7296,
                "height": 16340,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 44463,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 8394,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 31698,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 35914,
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
        "name": "Item-5",
        "description": "Item-5 Description",
        "parentId": null,
        "images": [
            {
                "id": 19,
                "name": "0019.jpg",
                "size": 10438,
                "primary": 1
            },
            {
                "id": 20,
                "name": "0020.jpg",
                "size": 17796,
                "primary": 0
            },
            {
                "id": 21,
                "name": "0021.jpg",
                "size": 22667,
                "primary": 0
            }
        ],
        "country": "AUD",
        "price": 5.5,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastUpdate": "2020-03-23T06:51:25.000Z",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 16862"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 77974"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 13551
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
                "value": 5924.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 61964,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 82178,
                "width": 92455,
                "height": 26599,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 75901,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 5126,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 41239,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 17998,
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
        "name": "Item-6",
        "description": "Item-6 Description",
        "parentId": null,
        "images": [
            {
                "id": 22,
                "name": "0022.jpg",
                "size": 257902,
                "primary": 1
            },
            {
                "id": 23,
                "name": "0023.jpg",
                "size": 37701,
                "primary": 0
            },
            {
                "id": 24,
                "name": "0024.jpg",
                "size": 81916,
                "primary": 0
            }
        ],
        "country": "AUD",
        "price": 6.6,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastUpdate": "2020-03-23T06:51:25.000Z",
        "children": []
    },
    {
        "1": {
            "attributeId": 1,
            "val": {
                "type": "string",
                "value": "some string 43314"
            }
        },
        "2": {
            "attributeId": 2,
            "val": {
                "type": "text",
                "value": "some text 99952"
            }
        },
        "3": {
            "attributeId": 3,
            "val": {
                "type": "number",
                "value": 81839
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
                "value": 37434.1,
                "country": "AUD"
            }
        },
        "6": {
            "attributeId": 6,
            "val": {
                "type": "volume",
                "value": 74415,
                "unit": "l"
            }
        },
        "7": {
            "attributeId": 7,
            "val": {
                "type": "dimension",
                "length": 16463,
                "width": 5584,
                "height": 45196,
                "unit": "cm"
            }
        },
        "8": {
            "attributeId": 8,
            "val": {
                "type": "area",
                "value": 49795,
                "unit": "cm"
            }
        },
        "9": {
            "attributeId": 9,
            "val": {
                "type": "length",
                "value": 12388,
                "unit": "cm"
            }
        },
        "10": {
            "attributeId": 10,
            "val": {
                "type": "width",
                "value": 63425,
                "unit": "cm"
            }
        },
        "11": {
            "attributeId": 11,
            "val": {
                "type": "height",
                "value": 60607,
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
        "name": "Item-7",
        "description": "Item-7 Description",
        "parentId": null,
        "images": [
            {
                "id": 25,
                "name": "0025.jpg",
                "size": 29061,
                "primary": 1
            },
            {
                "id": 26,
                "name": "0026.jpg",
                "size": 761031,
                "primary": 0
            },
            {
                "id": 27,
                "name": "0027.jpg",
                "size": 33368,
                "primary": 0
            }
        ],
        "country": "AUD",
        "price": 7.7,
        "creationDate": "2020-03-23T06:51:25.000Z",
        "lastUpdate": "2020-03-23T06:51:25.000Z",
        "children": []
    }
]
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



