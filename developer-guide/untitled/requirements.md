---
description: Application Installation instructions
---

# Dev - Installation

{% hint style="info" %}
You will need a database ready as well. See [here](dev-database/) for a database setup.
{% endhint %}

## Get the source code

Obtain the source code through either one of the following ways:

### Fork the repository from GitHub \(Preferred way, if you plan to contribute\)

This would be the preferred way if you would like to contribute to the code base.

See [Step 1 on how to fork and setup a forked repository](../../how-to-contribute.md).

### Downloading distribution Zip File

In [https://github.com/tmjeee/fuyuko](https://github.com/tmjeee/fuyuko) GitHub, at the top right corner click clone or download.



![](../../.gitbook/assets/image%20%2817%29.png)

Unzip downloaded fuyuko zip file \(eg. fuyuko-1.0.0.zip\) downloaded

```
$> unzip fuyuko-1.0.0.zip 
```

### Clone repository from GitHub

In [https://github.com/tmjeee/fuyuko](https://github.com/tmjeee/fuyuko) GitHub, at the top right corner click clone or download.

![](../../.gitbook/assets/image%20%2817%29.png)

Clone the repository through the following command

```text
$> git clone https://github.com/tmjeee/fuyuko.git
```

## Source code structure

Source code will have the following structure :

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
node src/app.js --db-host="mariadb"
```

{% hint style="info" %}
There should be no spaces between `=` and both `<config-name>` and `<config-value>`. See [here](dev-back-end/dev-be-configuration.md) for more information regarding configuration and its properties
{% endhint %}

### Configurations

Make sure configurations in `src/config/config.json` is being setup accordingly. See [here](dev-front-end/dev-fe-configuration.md) for more info about the possible configuration options.

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

### Configurations

Setup the configurations in `src/config/config.json` accodingly. See [here](dev-back-end/dev-be-configuration.md) for more information about the configuration options.

