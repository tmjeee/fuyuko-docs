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

`View` is the top most concept in the application. Almost everything revolves around the view \(item, attributes, pricing etc\) apart from user, group and roles. Information inside a view cannot be transfer or applied to a differrent view. 

`View` contains `Item`, `Attributes` and `Pricing` information. `Validations`, `Bulk Edits`, `Build-In Import`, `Build-In Export`, `Custom Import` and `Custom Export` applies to a particular `View` as well.

See [here](view.md) for more info.

### Items

`Items` lie inside a `View`. `Item` is hierarchical, it can contains other Items as children. `Item` can contains `Attributes`. `Item` has a _name_, which must be **unique** across the `View` it is in, a _description_ and **multiple** `Images`, of which only **one** an be the primary Image.

See [here](item.md) for more info about managing `Items`.

### Attributes

`Attributes` belongs to `Item`. Followings are the `Attributes` currently available.

{% hint style="info" %}
The difference between `text` and `string` is that `string` is represented with a HTML text field whereas text with HTML text area.
{% endhint %}

| Attribute | Description |
| :--- | :--- |
| `string` | Any characters representation.  |
| `text` | Any characters representation |
| `number` | Numeric representation |
| `date` | Date  |
| `currency` | Currency, amount in numeric format with country of the currency |
| `volume` | Volume, represented by a number and a unit of measurement |
| `dimension` | Dimension, length, width and height represented by number and a unit of measurement |
| `area` | Area, represented by number and a unit of measurement |
| `width` | Width, represented by number and a unit of measurement |
| `length` | Length, represented by a number and a unit of measurement |
| `height` | Height, represented by a number and a unit of measurement |
| `select` | A drop down list of text, where only one can be selected |
| `doubleselect` | Two drop down list of text, where only one can be selected on both. The second drop down list depends on the first. |

## Rules and Validations

Rules can be defined for a view. Rules can be either 

### Built-in Rules

These are rules with predefined options where one can select to build up the rules. They are made up of

#### Where clauses

Dictates when the validation should take place. It shall take place when all the where clauses are matched. A where clause is made up of 

#### Validate clauses

Dictates what attribute to be valIdated and what are the valid value of that attribute.

<table>
  <thead>
    <tr>
      <th style="text-align:left">Where / Validate Clause Components</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Attribute</td>
      <td style="text-align:left">The attribute to apply to</td>
    </tr>
    <tr>
      <td style="text-align:left">Operator</td>
      <td style="text-align:left">
        <p>Operator eg.</p>
        <ul>
          <li>equal (eq)</li>
          <li>not equal (not eq)</li>
          <li>less than (lt)</li>
          <li>not less than (not lt)</li>
          <li>greater than (gt)</li>
          <li>not greater than (not gt)</li>
          <li>greater than or equals (gte)</li>
          <li>not greater than or equals (not gte)</li>
          <li>less than or equals (lte)</li>
          <li>not less than or equals (not lte)</li>
          <li>empty (empty)</li>
          <li>not empty (not empty)</li>
          <li>contain (contain)</li>
          <li>not contain (not contain)</li>
          <li>regular expression (regexp)</li>
        </ul>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">Operand / Value</td>
      <td style="text-align:left">Values depending on the operator</td>
    </tr>
  </tbody>
</table>{% hint style="info" %}
Built-in validator basically allows one to say 

**When** `<attribute1> <operator1>` `<operand1>` is true, **validate** that `<attribute2>`  `<operator2>` `<operand2>` is true.

Eg. **When** `"attribute 1"` `"equals"` "`AUS"`, **validate** that `"attribute 2"` `"equals" "USD"` etc.
{% endhint %}

{% hint style="info" %}
* Operator that could be applied depends on the Attribute's Type
* Operand depends on the Operator

It should be obvious in the UI, as invalid operators and operand will not show up when they are invalid.
{% endhint %}

### Custom Validation

This would require writing scripts that perform certain validation operation and registering the results / error found. This would require technical skills and certain installation steps to be performed to installed it before it can show up in the application for user selection. See [here](../../developer-guide/untitled/dev-back-end/dev-be-custom-rule.md) for more info about setting it up.

See setting up [rules](rules.md) and running [validations](validation.md) based on them in the application.

## Pricing Structures



## Data Import and Export

## Bulk Edit

## Themes

## Dashboard and Widgets

## Trading Partners





