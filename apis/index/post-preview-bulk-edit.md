---
description: Bulk Edit Preview
---

# POST-preview-bulk-edit

{% api-method method="post" host="https://<host>:<port>/api/v1" path="/view/:viewId/preview-bulk-edit" %}
{% api-method-summary %}
Request a bulk edit preview
{% endapi-method-summary %}

{% api-method-description %}
Preview a bulk edit.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-headers %}
{% api-method-parameter name="x-auth-jwt" type="string" required=true %}
Authentication token.
{% endapi-method-parameter %}
{% endapi-method-headers %}

{% api-method-body-parameters %}
{% api-method-parameter name="changeClauses" type="array" required=true %}
Change clauses
{% endapi-method-parameter %}

{% api-method-parameter name="whenClauses" type="array" required=true %}
When clauses
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
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
  "payload": {
    "changeAttributes": [
        {
            "id": 4,
            "name": "date attribute",
            "description": "date attribute description",
            "type": "date",
            "format": "DD-MM-YYYY"
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
        }
    ],
    "whenAttributes": [
        {
            "id": 1,
            "name": "string attribute",
            "description": "string attribute 2222 description",
            "type": "string"
        },
        {
            "id": 4,
            "name": "date attribute",
            "description": "date attribute description",
            "type": "date",
            "format": "DD-MM-YYYY"
        }
    ],
    "bulkEditItems": [
        {
            "id": 1,
            "name": "name xxx",
            "description": "description xxx",
            "children": [
                {
                    "id": 2,
                    "name": "Item-1-1",
                    "description": "Item-1-1 Description",
                    "children": [],
                    "images": [],
                    "changes": {
                        "2": {
                            "old": {
                                "attributeId": 2,
                                "val": {
                                    "type": "text",
                                    "value": "some text 49867"
                                }
                            },
                            "new": {
                                "attributeId": 2,
                                "val": {
                                    "type": "text",
                                    "value": "xxxxxx"
                                }
                            }
                        },
                        "3": {
                            "old": {
                                "attributeId": 3,
                                "val": {
                                    "type": "number",
                                    "value": 91159
                                }
                            },
                            "new": {
                                "attributeId": 3,
                                "val": {
                                    "type": "number",
                                    "value": 2.2
                                }
                            }
                        },
                        "4": {
                            "old": {
                                "attributeId": 4,
                                "val": {
                                    "type": "date",
                                    "value": "12-10-1988"
                                }
                            },
                            "new": {
                                "attributeId": 4,
                                "val": {
                                    "type": "date",
                                    "value": "12-12-2020"
                                }
                            }
                        }
                    },
                    "whens": {
                        "1": {
                            "attributeId": 1,
                            "operator": "not empty",
                            "val": null
                        },
                        "4": {
                            "attributeId": 4,
                            "operator": "not eq",
                            "val": {
                                "type": "date",
                                "value": "12-12-2020"
                            }
                        }
                    }
                },
                {
                    "id": 3,
                    "name": "Item-1-2",
                    "description": "Item-1-2 Description",
                    "children": [],
                    "images": [],
                    "changes": {
                        "2": {
                            "old": {
                                "attributeId": 2,
                                "val": {
                                    "type": "text",
                                    "value": "some text 5756"
                                }
                            },
                            "new": {
                                "attributeId": 2,
                                "val": {
                                    "type": "text",
                                    "value": "xxxxxx"
                                }
                            }
                        },
                        "3": {
                            "old": {
                                "attributeId": 3,
                                "val": {
                                    "type": "number",
                                    "value": 84056
                                }
                            },
                            "new": {
                                "attributeId": 3,
                                "val": {
                                    "type": "number",
                                    "value": 2.2
                                }
                            }
                        },
                        "4": {
                            "old": {
                                "attributeId": 4,
                                "val": {
                                    "type": "date",
                                    "value": "12-10-1988"
                                }
                            },
                            "new": {
                                "attributeId": 4,
                                "val": {
                                    "type": "date",
                                    "value": "12-12-2020"
                                }
                            }
                        }
                    },
                    "whens": {
                        "1": {
                            "attributeId": 1,
                            "operator": "not empty",
                            "val": null
                        },
                        "4": {
                            "attributeId": 4,
                            "operator": "not eq",
                            "val": {
                                "type": "date",
                                "value": "12-12-2020"
                            }
                        }
                    }
                }
            ],
            "images": [],
            "changes": {
                "2": {
                    "old": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "some text 46581"
                        }
                    },
                    "new": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "xxxxxx"
                        }
                    }
                },
                "3": {
                    "old": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 10061
                        }
                    },
                    "new": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 2.2
                        }
                    }
                },
                "4": {
                    "old": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-10-1988"
                        }
                    },
                    "new": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-12-2020"
                        }
                    }
                }
            },
            "whens": {
                "1": {
                    "attributeId": 1,
                    "operator": "not empty",
                    "val": null
                },
                "4": {
                    "attributeId": 4,
                    "operator": "not eq",
                    "val": {
                        "type": "date",
                        "value": "12-12-2020"
                    }
                }
            }
        },
        {
            "id": 4,
            "name": "Item-2",
            "description": "Item-2 Description",
            "children": [],
            "images": [],
            "changes": {
                "2": {
                    "old": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "some text 21912"
                        }
                    },
                    "new": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "xxxxxx"
                        }
                    }
                },
                "3": {
                    "old": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 85954
                        }
                    },
                    "new": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 2.2
                        }
                    }
                },
                "4": {
                    "old": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-10-1988"
                        }
                    },
                    "new": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-12-2020"
                        }
                    }
                }
            },
            "whens": {
                "1": {
                    "attributeId": 1,
                    "operator": "not empty",
                    "val": null
                },
                "4": {
                    "attributeId": 4,
                    "operator": "not eq",
                    "val": {
                        "type": "date",
                        "value": "12-12-2020"
                    }
                }
            }
        },
        {
            "id": 5,
            "name": "Item-3",
            "description": "Item-3 Description",
            "children": [],
            "images": [],
            "changes": {
                "2": {
                    "old": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "some text 13189"
                        }
                    },
                    "new": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "xxxxxx"
                        }
                    }
                },
                "3": {
                    "old": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 23679
                        }
                    },
                    "new": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 2.2
                        }
                    }
                },
                "4": {
                    "old": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-10-1988"
                        }
                    },
                    "new": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-12-2020"
                        }
                    }
                }
            },
            "whens": {
                "1": {
                    "attributeId": 1,
                    "operator": "not empty",
                    "val": null
                },
                "4": {
                    "attributeId": 4,
                    "operator": "not eq",
                    "val": {
                        "type": "date",
                        "value": "12-12-2020"
                    }
                }
            }
        },
        {
            "id": 6,
            "name": "Item-4",
            "description": "Item-4 Description",
            "children": [],
            "images": [],
            "changes": {
                "2": {
                    "old": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "some text 26099"
                        }
                    },
                    "new": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "xxxxxx"
                        }
                    }
                },
                "3": {
                    "old": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 95086
                        }
                    },
                    "new": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 2.2
                        }
                    }
                },
                "4": {
                    "old": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-10-1988"
                        }
                    },
                    "new": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-12-2020"
                        }
                    }
                }
            },
            "whens": {
                "1": {
                    "attributeId": 1,
                    "operator": "not empty",
                    "val": null
                },
                "4": {
                    "attributeId": 4,
                    "operator": "not eq",
                    "val": {
                        "type": "date",
                        "value": "12-12-2020"
                    }
                }
            }
        },
        {
            "id": 7,
            "name": "Item-5",
            "description": "Item-5 Description",
            "children": [],
            "images": [],
            "changes": {
                "2": {
                    "old": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "some text 72480"
                        }
                    },
                    "new": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "xxxxxx"
                        }
                    }
                },
                "3": {
                    "old": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 90914
                        }
                    },
                    "new": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 2.2
                        }
                    }
                },
                "4": {
                    "old": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-10-1988"
                        }
                    },
                    "new": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-12-2020"
                        }
                    }
                }
            },
            "whens": {
                "1": {
                    "attributeId": 1,
                    "operator": "not empty",
                    "val": null
                },
                "4": {
                    "attributeId": 4,
                    "operator": "not eq",
                    "val": {
                        "type": "date",
                        "value": "12-12-2020"
                    }
                }
            }
        },
        {
            "id": 8,
            "name": "Item-6",
            "description": "Item-6 Description",
            "children": [],
            "images": [],
            "changes": {
                "2": {
                    "old": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "some text 21693"
                        }
                    },
                    "new": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "xxxxxx"
                        }
                    }
                },
                "3": {
                    "old": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 22831
                        }
                    },
                    "new": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 2.2
                        }
                    }
                },
                "4": {
                    "old": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-10-1988"
                        }
                    },
                    "new": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-12-2020"
                        }
                    }
                }
            },
            "whens": {
                "1": {
                    "attributeId": 1,
                    "operator": "not empty",
                    "val": null
                },
                "4": {
                    "attributeId": 4,
                    "operator": "not eq",
                    "val": {
                        "type": "date",
                        "value": "12-12-2020"
                    }
                }
            }
        },
        {
            "id": 9,
            "name": "Item-7",
            "description": "Item-7 Description",
            "children": [],
            "images": [],
            "changes": {
                "2": {
                    "old": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "some text 46396"
                        }
                    },
                    "new": {
                        "attributeId": 2,
                        "val": {
                            "type": "text",
                            "value": "xxxxxx"
                        }
                    }
                },
                "3": {
                    "old": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 42031
                        }
                    },
                    "new": {
                        "attributeId": 3,
                        "val": {
                            "type": "number",
                            "value": 2.2
                        }
                    }
                },
                "4": {
                    "old": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-10-1988"
                        }
                    },
                    "new": {
                        "attributeId": 4,
                        "val": {
                            "type": "date",
                            "value": "12-12-2020"
                        }
                    }
                }
            },
            "whens": {
                "1": {
                    "attributeId": 1,
                    "operator": "not empty",
                    "val": null
                },
                "4": {
                    "attributeId": 4,
                    "operator": "not eq",
                    "val": {
                        "type": "date",
                        "value": "12-12-2020"
                    }
                }
            }
        }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% hint style="info" %}
Request body expect `changeClauses` and `whenClauses` attributes as JSON Array contaning `ChangeClause` and `WhenClause` respectively
{% endhint %}

