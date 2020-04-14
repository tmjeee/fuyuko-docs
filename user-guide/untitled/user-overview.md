# Overview

{% hint style="info" %}
This section of the documentation is intended for users of the application. If you wish to extend, bug fix or contribute to the source code in any ways, the [developer guide ](../../developer-guide/untitled/)would be a better spot to start exploring.
{% endhint %}

Fuyuko is a Master Data Management / Product Information Management web based software application. 

Following are the core concepts of the software.

## Authentication and authorisation

The general idea is to assign users into groups which contains roles, allowing them do perform certain operations. Currently the following groups are available :

| Group | Description |
| :--- | :--- |
| VIEW Group |  |
| EDIT Group |  |
| ADMIN Group |  |
| PARTNER Group |  |

See [here](user-roles-management.md) for more information on how to manage users, groups and roles.

## Self Registrations and Invitations

There are 2 ways for user to get themselves into the application

### 1\) Self Registration

User get to a link and register themself. They would then wait for an existing user with appropriate role to approve their self registration and subsequently assigning them into appropriate group. See [here](registering-request-access/self-registration.md) for more info about self registration.

### 2\) Through an invitation

An existing user with appropriate role would trigger an invitation email being sent to a potential user with group and roles predefined. Upon clicking on an activation link on the email the potential user will have their account created an activated in the application. See [here](registering-request-access/invitation-and-activation.md) for more info.

See [here](registering-request-access/) for more information.

## Views

View is the top most concept in the application. Almost everything revolves around the view \(item, attributes, pricing etc\) apart from user, group and roles. Information inside a view cannot be transfer or applied to a differrent view. 

View contains Item, attributes and pricing information. Validations, bulk edits, build in and custom import and exports applies to a particular view as well.

See [here](view.md) for more info.

## Items



## Attributes

## Rules and Validations

## Pricing Structures

## Data Import and Export

## Bulk Edit

## Themes

## Dashboard and Widgets

## Trading Partners





