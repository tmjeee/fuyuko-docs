---
description: Application Installation instructions
---

# Installation

## Prerequisite

Unzip downloaded fuyuko zip file \(eg. fuyuko-1.0.0.zip\) downloaded

```
$> unzip fuyuko-1.0.0.zip 
```

After unzip, the following folder structure will be observed

```text
+ fe/
   +-          ... content of front end code ...
+ be/
   +-          ... content of back end code ...
+ LICENSE      ... License ...
+ README.md    ... Readme file ...
```

## Front End Installation

Following instructions assume we are in `fe/` subdirectory of the root installation directory, if you are not cd into it using the following command

```text
$> cd fe/
```

To run in foreground

```text
$> npm run exec
```

To run in background

```text
$> npm run exec &
```

To override configurations in `config/config.json` where`<config-name>` is the config param name and `<config-value>` is the configuration parameter value in `config/config.json` respectively

```text
$> node src/app.js --<config-name>=<config-value>
```

Eg. the following would override `db-host` to `mariadb`

```text
node src/app.js --db-host=mariadb
```

{% hint style="info" %}
There should be no spaces between `=` and both `<config-name>` and `<config-value>`
{% endhint %}

## Back End Installation

Following instructions assume we are in b`e/` subdirectory of the root installation directory, if you are not cd into it using the following command

```text
$> cd be/
```

To run in foreground 

```text
$> ng serve
```

To run in background

```text
$> ng serve &
```

