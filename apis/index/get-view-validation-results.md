---
description: Get view validation results
---

# GET-view-validation-results

{% api-method method="get" host="https://<host>:<port>/api/v1" path="/view/:viewId/validation/:validationId" %}
{% api-method-summary %}
Get view validation results
{% endapi-method-summary %}

{% api-method-description %}
Get View's validation result.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="viewId" type="number" required=true %}
View Id
{% endapi-method-parameter %}

{% api-method-parameter name="validationId" type="number" required=true %}
Validation Id
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
  "payload": {
    "id": 1,
    "viewId": 1,
    "name": "test view1 vaslidation",
    "description": "asdsdsd",
    "progress": "COMPLETED",
    "creationDate": "2020-03-25T13:42:20.000Z",
    "lastUpdate": "2020-03-25T13:42:22.000Z",
    "logs": [
        {
            "id": 1,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Running Predefined Rules validations for viewId 1 validationId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 2,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved validation for validationId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 3,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved attributes for viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 4,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved all items for viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 5,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved all rules for viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 6,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=unknown] \n             - Validating itemId 1 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 7,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validating WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 8,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 9,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating ValidateClause 1 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 10,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 1 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 11,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ValidateClauses for ruleId 1 on itemId 1 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 12,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ItemId 1 FAILED ruleId 1 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 13,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating itemId 1 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 14,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validating WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 15,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 16,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating ValidateClause 2 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 17,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 2 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 18,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ValidateClauses for ruleId 2 on itemId 1 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 19,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ItemId 1 FAILED ruleId 2 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 20,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating itemId 1 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 21,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validating WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 22,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 23,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating ValidateClause 3 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 24,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 3 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 25,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ValidateClauses for ruleId 3 on itemId 1 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 26,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ItemId 1 FAILED ruleId 3 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 27,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating itemId 1 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 28,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validating WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 29,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 30,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating ValidateClause 4 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 31,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 4 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 32,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ValidateClauses for ruleId 4 on itemId 1 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 33,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ItemId 1 FAILED ruleId 4 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 34,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating itemId 1 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 35,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validating WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 36,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 37,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating ValidateClause 5 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 38,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 5 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 39,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ValidateClauses for ruleId 5 on itemId 1 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 40,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ItemId 1 FAILED ruleId 5 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 41,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating itemId 1 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 42,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validating WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 43,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 1 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 44,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validating ValidateClause 6 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 45,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 6 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 1 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 46,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ValidateClauses for ruleId 6 on itemId 1 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 47,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=1]\n             [attributeId=1] \n             - ItemId 1 FAILED ruleId 6 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 48,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating itemId 4 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 49,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validating WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 50,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 51,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating ValidateClause 1 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 52,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 1 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 53,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ValidateClauses for ruleId 1 on itemId 4 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 54,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ItemId 4 FAILED ruleId 1 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 55,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating itemId 4 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 56,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validating WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 57,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 58,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating ValidateClause 2 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 59,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 2 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 60,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ValidateClauses for ruleId 2 on itemId 4 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 61,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ItemId 4 FAILED ruleId 2 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 62,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating itemId 4 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 63,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validating WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 64,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 65,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating ValidateClause 3 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 66,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 3 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 67,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ValidateClauses for ruleId 3 on itemId 4 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 68,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ItemId 4 FAILED ruleId 3 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 69,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating itemId 4 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 70,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validating WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 71,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 72,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating ValidateClause 4 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 73,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 4 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 74,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ValidateClauses for ruleId 4 on itemId 4 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 75,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ItemId 4 FAILED ruleId 4 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 76,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating itemId 4 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 77,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validating WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 78,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 79,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating ValidateClause 5 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 80,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 5 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 81,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ValidateClauses for ruleId 5 on itemId 4 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 82,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ItemId 4 FAILED ruleId 5 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 83,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating itemId 4 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 84,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validating WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 85,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 4 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 86,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validating ValidateClause 6 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 87,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 6 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 4 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 88,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ValidateClauses for ruleId 6 on itemId 4 is FALSE",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 89,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=4]\n             [attributeId=1] \n             - ItemId 4 FAILED ruleId 6 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 90,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating itemId 5 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 91,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validating WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:20.000Z"
        },
        {
            "id": 92,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 93,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating ValidateClause 1 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 94,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 1 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 95,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ValidateClauses for ruleId 1 on itemId 5 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 96,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ItemId 5 FAILED ruleId 1 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 97,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating itemId 5 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 98,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validating WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 99,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 100,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating ValidateClause 2 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 101,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 2 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 102,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ValidateClauses for ruleId 2 on itemId 5 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 103,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ItemId 5 FAILED ruleId 2 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 104,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating itemId 5 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 105,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validating WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 106,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 107,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating ValidateClause 3 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 108,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 3 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 109,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ValidateClauses for ruleId 3 on itemId 5 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 110,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ItemId 5 FAILED ruleId 3 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 111,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating itemId 5 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 112,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validating WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 113,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 114,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating ValidateClause 4 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 115,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 4 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 116,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ValidateClauses for ruleId 4 on itemId 5 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 117,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ItemId 5 FAILED ruleId 4 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 118,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating itemId 5 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 119,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validating WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 120,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 121,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating ValidateClause 5 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 122,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 5 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 123,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ValidateClauses for ruleId 5 on itemId 5 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 124,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ItemId 5 FAILED ruleId 5 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 125,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating itemId 5 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 126,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validating WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 127,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 5 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 128,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validating ValidateClause 6 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 129,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 6 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 5 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 130,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ValidateClauses for ruleId 6 on itemId 5 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 131,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=5]\n             [attributeId=1] \n             - ItemId 5 FAILED ruleId 6 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 132,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating itemId 6 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 133,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validating WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 134,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 135,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating ValidateClause 1 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 136,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 1 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 137,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ValidateClauses for ruleId 1 on itemId 6 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 138,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ItemId 6 FAILED ruleId 1 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 139,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating itemId 6 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 140,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validating WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 141,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 142,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating ValidateClause 2 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 143,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 2 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 144,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ValidateClauses for ruleId 2 on itemId 6 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 145,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ItemId 6 FAILED ruleId 2 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 146,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating itemId 6 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 147,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validating WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 148,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 149,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating ValidateClause 3 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 150,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 3 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 151,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ValidateClauses for ruleId 3 on itemId 6 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 152,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ItemId 6 FAILED ruleId 3 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 153,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating itemId 6 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 154,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validating WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 155,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 156,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating ValidateClause 4 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 157,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 4 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 158,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ValidateClauses for ruleId 4 on itemId 6 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 159,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ItemId 6 FAILED ruleId 4 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 160,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating itemId 6 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 161,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validating WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 162,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 163,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating ValidateClause 5 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 164,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 5 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 165,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ValidateClauses for ruleId 5 on itemId 6 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 166,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ItemId 6 FAILED ruleId 5 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 167,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating itemId 6 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 168,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validating WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 169,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 6 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 170,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validating ValidateClause 6 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 171,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 6 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 6 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 172,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ValidateClauses for ruleId 6 on itemId 6 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 173,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=6]\n             [attributeId=1] \n             - ItemId 6 FAILED ruleId 6 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 174,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating itemId 7 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 175,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validating WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 176,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 177,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating ValidateClause 1 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 178,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 1 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 179,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ValidateClauses for ruleId 1 on itemId 7 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 180,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ItemId 7 FAILED ruleId 1 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 181,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating itemId 7 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 182,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validating WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 183,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 184,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating ValidateClause 2 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 185,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 2 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 186,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ValidateClauses for ruleId 2 on itemId 7 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 187,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ItemId 7 FAILED ruleId 2 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 188,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating itemId 7 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 189,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validating WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 190,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 191,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating ValidateClause 3 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 192,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 3 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 193,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ValidateClauses for ruleId 3 on itemId 7 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 194,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ItemId 7 FAILED ruleId 3 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 195,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating itemId 7 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 196,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validating WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 197,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 198,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating ValidateClause 4 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 199,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 4 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 200,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ValidateClauses for ruleId 4 on itemId 7 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 201,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ItemId 7 FAILED ruleId 4 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 202,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating itemId 7 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 203,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validating WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 204,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 205,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating ValidateClause 5 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 206,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 5 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 207,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ValidateClauses for ruleId 5 on itemId 7 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 208,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ItemId 7 FAILED ruleId 5 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 209,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating itemId 7 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 210,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validating WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 211,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 7 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 212,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validating ValidateClause 6 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 213,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 6 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 7 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 214,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ValidateClauses for ruleId 6 on itemId 7 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 215,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=7]\n             [attributeId=1] \n             - ItemId 7 FAILED ruleId 6 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 216,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating itemId 8 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 217,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validating WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 218,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 219,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating ValidateClause 1 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 220,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 1 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 221,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ValidateClauses for ruleId 1 on itemId 8 is FALSE",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 222,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ItemId 8 FAILED ruleId 1 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 223,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating itemId 8 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 224,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validating WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:21.000Z"
        },
        {
            "id": 225,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 226,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating ValidateClause 2 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 227,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 2 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 228,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ValidateClauses for ruleId 2 on itemId 8 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 229,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ItemId 8 FAILED ruleId 2 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 230,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating itemId 8 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 231,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validating WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 232,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 233,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating ValidateClause 3 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 234,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 3 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 235,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ValidateClauses for ruleId 3 on itemId 8 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 236,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ItemId 8 FAILED ruleId 3 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 237,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating itemId 8 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 238,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validating WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 239,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 240,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating ValidateClause 4 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 241,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 4 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 242,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ValidateClauses for ruleId 4 on itemId 8 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 243,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ItemId 8 FAILED ruleId 4 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 244,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating itemId 8 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 245,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validating WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 246,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 247,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating ValidateClause 5 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 248,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 5 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 249,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ValidateClauses for ruleId 5 on itemId 8 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 250,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ItemId 8 FAILED ruleId 5 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 251,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating itemId 8 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 252,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validating WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 253,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 8 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 254,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validating ValidateClause 6 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 255,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 6 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 8 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 256,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ValidateClauses for ruleId 6 on itemId 8 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 257,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=8]\n             [attributeId=1] \n             - ItemId 8 FAILED ruleId 6 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 258,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating itemId 9 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 259,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validating WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 260,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 1 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 261,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating ValidateClause 1 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 262,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 1 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 1 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 263,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ValidateClauses for ruleId 1 on itemId 9 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 264,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ItemId 9 FAILED ruleId 1 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 265,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating itemId 9 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 266,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validating WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 267,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 2 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 268,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating ValidateClause 2 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 269,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 2 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 2 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 270,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ValidateClauses for ruleId 2 on itemId 9 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 271,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ItemId 9 FAILED ruleId 2 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 272,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating itemId 9 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 273,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validating WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 274,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 3 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 275,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating ValidateClause 3 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 276,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 3 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 3 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 277,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ValidateClauses for ruleId 3 on itemId 9 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 278,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ItemId 9 FAILED ruleId 3 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 279,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating itemId 9 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 280,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validating WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 281,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 4 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 282,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating ValidateClause 4 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 283,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 4 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 4 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 284,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ValidateClauses for ruleId 4 on itemId 9 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 285,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ItemId 9 FAILED ruleId 4 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 286,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating itemId 9 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 287,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validating WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 288,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 5 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 289,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating ValidateClause 5 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 290,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 5 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 5 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 291,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ValidateClauses for ruleId 5 on itemId 9 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 292,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ItemId 9 FAILED ruleId 5 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 293,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating itemId 9 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 294,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validating WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 295,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=2] \n             - Validated current WhenClause result is [true] overall WhenClause result is [true] for WhenClause 6 \n                           (attributeId 2 attributeName text attribute \n                           whenClause condition {type: text value: val text 1}{type: text value: val text 2}\n                           op not eq \n                           against itemValueTypes {type: text value: val text 1}{type: text value: val text 2})\n                           for itemId 9 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 296,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validating ValidateClause 6 \n                           (attributeId 1 attributeName string attribute op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 297,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - Validated current ValidateClause result is [false] overall ValidateClause result is [true] for ValidateClause 6 \n                           (attributeId 1 attributeName string attribute \n                           validateClause condition {type: string value: val string 1{type: string value: val string 2 \n                           op eq \n                           against itemValueTypes {type: string value: val string 1{type: string value: val string 2)\n                           for itemId 9 against ruleId 6 in viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 298,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ValidateClauses for ruleId 6 on itemId 9 is FALSE",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 299,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=9]\n             [attributeId=1] \n             - ItemId 9 FAILED ruleId 6 validation, error will be logged in db",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 300,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Running Custom Rule validations for viewId 1 validationId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 301,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieve view with id 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 302,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved validation for validationId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 303,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved attributes for viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 304,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved all items for viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 305,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved all custom rules for viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 306,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Successfully retrieved all rules for viewId 1",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 307,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Running against custom rule with id 1 named 0.0.1-sample-rule-1.js",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 308,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Running custom rule 0.0.1-sample-rule-1.js",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 309,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - End of custom rule 0.0.1-sample-rule-1.js run",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 310,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Running against custom rule with id 2 named 0.0.2-sample-rule-2.js",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 311,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - Running custom rule 0.0.2-sample-rule-2.js",
            "creationDate": "2020-03-25T13:42:22.000Z"
        },
        {
            "id": 312,
            "level": "INFO",
            "message": "[validationId=1]\n             [itemId=unknown]\n             [attributeId=unknown] \n             - End of custom rule 0.0.2-sample-rule-2.js run",
            "creationDate": "2020-03-25T13:42:22.000Z"
        }
    ],
    "errors": [
        {
            "id": 1,
            "itemId": 1,
            "ruleId": 1,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 154 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 2,
            "itemId": 1,
            "ruleId": 2,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 154 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 3,
            "itemId": 1,
            "ruleId": 3,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 154 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 4,
            "itemId": 1,
            "ruleId": 4,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 154 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 5,
            "itemId": 1,
            "ruleId": 5,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 154 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 6,
            "itemId": 1,
            "ruleId": 6,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 154 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 7,
            "itemId": 4,
            "ruleId": 1,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 18598 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 8,
            "itemId": 4,
            "ruleId": 2,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 18598 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 9,
            "itemId": 4,
            "ruleId": 3,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 18598 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 10,
            "itemId": 4,
            "ruleId": 4,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 18598 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 11,
            "itemId": 4,
            "ruleId": 5,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 18598 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 12,
            "itemId": 4,
            "ruleId": 6,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 18598 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 13,
            "itemId": 5,
            "ruleId": 1,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 85614 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 14,
            "itemId": 5,
            "ruleId": 2,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 85614 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 15,
            "itemId": 5,
            "ruleId": 3,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 85614 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 16,
            "itemId": 5,
            "ruleId": 4,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 85614 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 17,
            "itemId": 5,
            "ruleId": 5,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 85614 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 18,
            "itemId": 5,
            "ruleId": 6,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 85614 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 19,
            "itemId": 6,
            "ruleId": 1,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 45119 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 20,
            "itemId": 6,
            "ruleId": 2,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 45119 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 21,
            "itemId": 6,
            "ruleId": 3,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 45119 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 22,
            "itemId": 6,
            "ruleId": 4,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 45119 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 23,
            "itemId": 6,
            "ruleId": 5,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 45119 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 24,
            "itemId": 6,
            "ruleId": 6,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 45119 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 25,
            "itemId": 7,
            "ruleId": 1,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 12687 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 26,
            "itemId": 7,
            "ruleId": 2,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 12687 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 27,
            "itemId": 7,
            "ruleId": 3,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 12687 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 28,
            "itemId": 7,
            "ruleId": 4,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 12687 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 29,
            "itemId": 7,
            "ruleId": 5,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 12687 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 30,
            "itemId": 7,
            "ruleId": 6,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 12687 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 31,
            "itemId": 8,
            "ruleId": 1,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 16862 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 32,
            "itemId": 8,
            "ruleId": 2,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 16862 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 33,
            "itemId": 8,
            "ruleId": 3,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 16862 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 34,
            "itemId": 8,
            "ruleId": 4,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 16862 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 35,
            "itemId": 8,
            "ruleId": 5,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 16862 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 36,
            "itemId": 8,
            "ruleId": 6,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 16862 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 37,
            "itemId": 9,
            "ruleId": 1,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 43314 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 38,
            "itemId": 9,
            "ruleId": 2,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 43314 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 39,
            "itemId": 9,
            "ruleId": 3,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 43314 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 40,
            "itemId": 9,
            "ruleId": 4,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 43314 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 41,
            "itemId": 9,
            "ruleId": 5,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 43314 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        },
        {
            "id": 42,
            "itemId": 9,
            "ruleId": 6,
            "attributeId": 1,
            "message": "Attribute string attribute (1) value {type: string value: some string 43314 eq {type: string value: val string 1{type: string value: val string 2 FAILED "
        }
    ]
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



