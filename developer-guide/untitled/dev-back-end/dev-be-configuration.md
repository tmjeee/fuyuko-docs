# Dev - BE - Configuration

## Configurations

Follwowing is the configuration file, `config.json`,  located in `/src/config/`

```text
{
  "db-host": "localhost",
  "db-user": "root",
  "db-password": "root",
  "db-port": 3306,
  "db-database": "fuyuko",
  "version": "1.0.0-beta",
  "port": 8888,

  "timezone": "Australia/Sydney",

  "updater-run": true,
  "updater-profiles": ["CORE", "TEST-DATA", "CARS-DATA", "LEEFAHMEE-DATA"],
  "updater-profiles-help": "Available updater profiles are CORE, TEST-DATA, CARS-DATA, LEEFAHMEE-DATA",

  "salt": "some-salt",

  "jwt-secret": "some-secret",
  "jwt-expiration": "5h",

  "fe-url-base": "http://localhost:4200",
  "help-url-base": "https://raw.githubusercontent.com/tmjeee/fuyuko-app-docs/v1.0.0",

  "request-payload-limit": "900mb",

  "smtp-host": "smtp.gmail.com",
  "smtp-port": 587,
  "smtp-secure": false,
  "smtp-user": "fuyuko.mdm@gmail.com",
  "smtp-password": "",
  "smtp-from-email": "app@fuyuko.com",

  "default-theme": "deeppurple_amber_light"
}

```

| Config Property | Description |
| :--- | :--- |
| db-host | Mariadb / MySQL Database host name or ip |
| db-user | Mariadb / MySQL Database username |
| db-password | Mariadb / MySQL Database password |
| db-database | Mariadb / MySQL Database name |
| verison | version of Fuyuko distribution |
| timezone | Timezone used |
| updater-run | true or false to run updater on bootup |
| updater-profiles | Profiles to run on bootup \(see following Profiles section for more info\) |
| port | port number where the API server will expose it's service |
| salt | Password salt to use |
| jwt-secret | jwt secret to use |
| jwt-expiration | jwt expiration \(when remember me is selected only\) |
| fe-url-base | URL where the Front End is hosted |
| help-url-base | URL where help files are stored |
| request-payload-limit | Limit of file upload allowed |
| smtp-host | SMTP server host name or ip |
| smtp-port | SMTP server port number |
| smtp-secure | SMTP connection to be secure \(true or false\) |
| smtp-user | SMTP server logon username |
| smtp-password | SMTP server logon password |
| smtp-from-email | SMTP from email to use |
| default-theme | Default theme \(see Themes section below for more info\) |

## Overriding configurations 

Configurations can be overriden at command line eg.

```text
$> node app.js --db-user="myUser" --db-password="myPass"
```

would override `db-user` and `db-password` config properties to `myUser` and `myPass` respectively.

{% hint style="info" %}
* Note the double quotes, they are parsed, so the double quotes are needed to indicate it is string, similarly `["one","two"]` would be parsed to array of `strings` as some config properties takes in array of `strings` eg. `updater-profiles`
* Note that there is no space on both left and right of the `=`, it needs to be `<config_property>=<config_value>`
{% endhint %}

## Profiles

| Profile Name | Description |
| :--- | :--- |
| CORE | Contains scripts / code needed to ensure proper running / bootup of the system. **THIS PROFILE IS MANDATORY.** |
| TEST-DATA | Contains scripts / code needed to setup test data. This data is required to run tests. This data is good for testing the system. **THIS PROFILE IS OPTIONAL**. |
| CARS-DATA | Contains scripts / code needed to setup a `Cars` profile. It contains massive data, about 2064 items. You will need to wait for quite a while if you include this profile. This is good for testing the performance of the system. **THIS PROFILE IS OPTIONAL.** |
| LEEFAHMEE-DATA | Contains scripts / code needed to setup a  `Lee Fah Mee` profile. It contains items for [Lee Fah Mee](http://www.leefahmee.com.my/products/). This represents a somewhat slightly more realistic real world data. **THIS PROFILE IS OPTIONAL.** |

## Themes

| Theme |  |
| :--- | :--- |
| THEME\_DEEPPURPLE\_AMBER\_LIGHT | Deep Purple Amber Light Theme |
| THEME\_DEEPPURPLE\_AMBER\_DARK | Deep Purple Amber Dark Theme |
| THEME\_INDIGO\_PINK\_LIGHT | Indigo Pink Light Theme |
| THEME\_INDIGO\_PINK\_DARK | Indigo Pink Dark Theme |
| THEME\_PINK\_BLUEGREY\_LIGHT | Pink Bluegrey Light Theme |
| THEME\_PINK\_BLUEGREY\_DARK | Pink BlueGrey Dark Theme |
| THEME\_PURPLE\_GREEN\_LIGHT | Purple Green Light Theme |
| THEME\_PURPLE\_GREEN\_DARK | Purple Green Dark Theme |
| THEME\_INDIGO\_LIGHTBLUE\_LIGHT | Indigo Lightblue Light Theme |
| THEME\_INDIGO\_LIGHTBLUE\_DARK | Indigo Lightblue Dark Theme |

