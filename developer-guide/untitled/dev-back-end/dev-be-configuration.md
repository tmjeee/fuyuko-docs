# Dev - BE - Configuration

## General configurations

Follwowing is the configuration file, `config.json`,  located in `/src/config/`

```text
{
  "db-host": "localhost",
  "db-user": "root",
  "db-password": "some-password",
  "db-port": 3306,
  "db-database": "fuyuko",
  "db-runUpdater": true,
  "version": "1.0.0-beta",
  "port": 8888,

  "salt": "some-salt",

  "jwt-secret": "some-secret",
  "jwt-expiration": "5h",

  "fe-url-base": "http://localhost:4200",
  "help-url-base": "https://raw.githubusercontent.com/tmjeee/fuyuko-app-docs/v1.0.0",

  "request-payload-limit": "900mb",

  "smtp-host": "smtp.your-company.com",
  "smtp-port": 587,
  "smtp-secure": false,
  "smtp-user": "some@email-address.com",
  "smtp-password": "oadgedcsksapsdpdcsy",
  "smtp-from-email": "some@email-address.com",

  "default-theme": "deeppurple_amber_light"
}

```

| Config Property | Description |
| :--- | :--- |
| db-host |  |
| db-user |  |
| db-password |  |
| db-database |  |
| db-runUpdater |  |
| verison |  |
| port |  |
| salt |  |
| jwt-secret |  |
| jwt-expiration |  |
| request-payload-limit |  |
| smtp-host |  |
| smtp-port |  |
| smtp-secure |  |
| smtp-user |  |
| smtp-password |  |
| smtp-from-email |  |
| default-theme |  |

## Overriding configurations 

Configurations can be overriden at command line eg.

```text
$> node app.js --db-user="myUser" --db-password="myPass"
```

would override `db-user` and `db-password` config properties to `myUser` and `myPass` respectively.

{% hint style="info" %}
* Note the double quotes, they are parsed, so the double quotes are needed to indicate it is string, similarly `["one","two"]` would be parsed to array of `strings` as some config properties takes in array of `strings` eg. `updater-profiles`
* Note that there is no space on both left and right of the `=`, it needs to be `<config_property>=<config_value_expression>`
{% endhint %}

