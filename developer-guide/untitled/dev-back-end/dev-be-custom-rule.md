# Dev - BE - Custom Rule

## Location

Located in `src/custom-rule`. Custom rule scripts needs to be dump in `src/custom-rule/rules` directory

## Script naming convention

Typically named `<semver-version-format>-<short-description-of-rule-function>.ts`

## Directory structure

```text
+ src/
  + custom-rule
    + rules/
       - 0.0.1-sample-rule-1.ts
       - 0.0.2-sample-rule-2.ts
```

* custom rule scripts should be located in src/custom-rule/rules directory
* adding new custom rule to the directory will need a restart of the back-end server so synchronisation can take place.
* removing a custom rule would require removing it from the directory and doing a restart of the back-end server for synchronisation to take place.
* Upon synchronisation, custom rules will be avialable in the application.

{% hint style="warning" %}
Warning

Removing and existing custom rule, will result in all it's information being lost
{% endhint %}

## Script synchronisation

Upon startup, the application will try to synchronise the custom rule scripts with the information it had in the database based on the following conditions:

1. If a custom rule script, identified by it's name exists in src/custom-rule/rules directory but do not exists in application database, one will be created
2. If a custom rule script, identifed by its name do not exists in src/custom-rule/rules directory but exists in application database, the one in application database will be wipe out.
3. If a custom rule script, identified by its name exists in src/custom-rule/rules directory and also exists in application database, no action is required, they are in sync.

## Script Structure

The name of the rule would be the filename of the custom rule script.

If you were to write a custom rule script , you would need to follow this structure.

 Typical custom rule script would look as follows :

```text
import {CustomValidationContext} from "../../model/validation.model";

export const description = (): string => {
    // a string description of the rule
    return `0.0.1 Sample Rule #1`;
}

export const run = (ctx: CustomValidationContext) => {
    // code to be executed when this custom rule is triggered
}

```

It would require :

### `description` function

Returns a description of the custom validation rule, typically what it does.

### `run` function

This is what gets call when this custom rule is triggered, it will contain code to do whatever this custom rule is meant to be validating. A `ctx` \(context\) will be available for the user to access the application.

Following are functions / properties inside a `ctx` :

#### `log(msg: string)` function

log messages

#### `viewId(): number` function

get viewId custom rule is operating on

#### `validationId(): number` function

get the validation id for this custom rule validation run

#### `itemId(): number` function

get the item id for the current custom rule validation run

#### `item(): Item` function

get the `Item` for the current custom rule validation run

#### `attribute(attributeId: number): Attribute` function

get the `Attribute` by attribute id

#### `reportError(attributeId: number, message: string): void` function

Report a validation error when validating the current `Item`'s `Attribute`

