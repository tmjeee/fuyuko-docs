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
| VIEW Group | Groups where members can view only operations in the system. |
| EDIT Group | Groups where members can perform actions in the system |
| ADMIN Group | Groups where members can perform higher order administration in the system. |
| PARTNER Group | Groups where members can access partner section and view prices for views configured. |

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

`Pricing Structures` are a way to group pricing in a `View`. A View can contain many `Pricing Structures`. Each `Pricing Structure` holds prices for all Items within that `View`. This way we can have `Pricing Structures` for different trading partners.

See [here](pricing-structure.md) for more info about the setup an usage of pricing structures.

## Data Import

There are 2 types of data import, see [here](import.md) for more info. All imports revolves importing into a particular `View`.

### Built-In Data Import

| Built-In Data Import Types | Description |
| :--- | :--- |
| Attributes Import | Import of `Attributes` in csv format, through a wizard like process in the application. |
| Items Import | Import of `Items` in csv format, through a wizard like process in the application. |
| Prices Import | Import of `Prices` in csv format, through a wizard like process in the application. |

### Custom Data Import

This would require some technical skills as it involves writting scripts that perform custom imports into the application. The script will need to be installed into the application \(see [here](../../developer-guide/untitled/dev-back-end/dev-be-custom-import.md) for more info\) before it is available for the user to select. The custom scripts will allow inputs of the following types to be created in the gather information for custom import

| Input types | Description |
| :--- | :--- |
| string | Text input |
| number | Number input |
| date | Date picker |
| checkbox | True or false checkbox |
| select | Drop down list with one possible selection |

## Data Export

There are 2 types of data export, see [here](export.md) for more info. All export revolves around exporting `Items`, `Attributes` and Prices of a particular `View`

### Build-In  Data Export

| Build-In Data Export Types | Description |
| :--- | :--- |
| Prices Export | Export of `Prices` in csv format through a wizard like proces in the application. |
| Attributes Export | Export of `Attributes` in csv format through a wizard like process in the application. |
| Items Export | Export of `Items` in csv format through a wizard like process in the application. |

### Custom Data Export

This would require some technical skills as it involves writting scripts that perform custom exports from `Views` of application. The script will need to be installed into the application \(see [here](../../developer-guide/untitled/dev-back-end/dev-be-custom-export.md) for more info\) before it is available for the user to select. The custom scripts will allow inputs of the following types to be created in the gather information for custom import

| Input types | Description |
| :--- | :--- |
| string | Text input |
| number | Number input |
| date | Date picker |
| checkbox | True or false checkbox |
| select | Drop down list with one possible selection |

## Bulk Edit

A wizard like a process to perform edit when conditions are met, see [here](bulk-edit.md) for more info. Made up of 

### Change Clause

Indicate what attribute\(s\) and its value\(s\) to change

| Change Clause |  |
| :--- | :--- |
| Attribute | Attribute to change |
| Value | The value to change it to |

### When Clause

Indicate when the change should take effect.

<table>
  <thead>
    <tr>
      <th style="text-align:left">When Clause Components</th>
      <th style="text-align:left"></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">Attribute</td>
      <td style="text-align:left">Attribute to check</td>
    </tr>
    <tr>
      <td style="text-align:left">Operator</td>
      <td style="text-align:left">
        <p>Operator</p>
        <p></p>
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
      <td style="text-align:left">Value the operator operates on to check for validity</td>
    </tr>
  </tbody>
</table>{% hint style="info" %}
Bulk edit is essentially telling the application " when `<attribute>` `<operator>` `<operand>` is true, change `<attribute value>` to `<new attribute value>`"

Eg. change all "currency code attribute" to "AUD" when "country code attribute" is "AUS"
{% endhint %}

## Themes

Each theme will have "dark" and "Light" mode. Theme availables are:

* Deeppurple Amber Light Theme
* Deeppurple Amber Dark Theme
* Indigo Pink Light Theme
* Indigo Pink Dark Theme
* Pink Bluegrey Light Theme
* Pink Bluegrey Dark Theme
* Purple Green Light Theme
* Purple Green Dark Theme
* Indigo Lightblue Light Theme
* Indigo Lightblue Dark Theme

## Dashboard and Widgets

Dashboard is basically a section where you can : 

* Select its layout, right now there are only 2 layouts
  * 1 column, where widget are stacked up
  * 2 columns, where widget can be stacked up on either left or right
  * See [here](../../developer-guide/untitled/dev-front-end/dev-fe-dashboard-and-widgets.md) for more information about creating a dashboard layout of your own
* Select widgets to display in the dashboard. 
  * Multiple instances of the same widgets are possible.
  * Widgets can be moved around by drag and drop
  * Removeable by click on the cross button which should appear when they are hovered over
  * See [here](../../developer-guide/untitled/dev-front-end/dev-fe-dashboard-and-widgets.md) for more information about creating a widget of your own

See [here](dashboard.md) for more information about configuring the layout and adding / removing widgets.

## Trading Partners

Trading partners are basically those user with ROLE\_PARTNER in the group they are in. This allow them access to the trading partner page where they can see prices of items based on Pricing Structure. Each trading partner can have one or many Pricing Structures assinged to them allowing them to see sets of items with potentially different prices. See [here](partner.md) for more information.



