# Dev - Database

{% hint style="info" %}
This software was designed to work with **MariaDB 10.x** or **MySQL 8.x** or their later derivatives
{% endhint %}

## Setting Time Zone 

As the application depends on database timezone, it is important to set time zone of your MariaDb or MySQL database timezone to be consistent with FE and BE. To set the time zone in Mariadb / MySQL.

Run the followings to import all the timezones into MariaDB / MySQL \(a one time only process\)

```text
$> mysql_tzinfo_to_sql /usr/share/zoneinfo | mariadb -u root mysql -p
```

Set the timezone through the following Query

```text
SET GLOBAL time_zone = 'Australia/Sydney';  # or whatever your timezone is
```

Standard timezone values can be found [here](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).

## Installing MariaDb

Assuming you are using ubuntu, MariaDB can be installed through the following command

```text
$> sudo apt install -y mariadb-server
```

## Creating a database 

Assuming you have a `root` in your database with a password set, you would need to do the following to get into MariaDb. Omit `-p` if you don't have a password for `root`.

```text
$> mariadb -u root -p 
```

Create a database called `fuyuko`, this is the default database, if it is not changed in BE's `config.json`

```text
$> create database fuyuko;
```

