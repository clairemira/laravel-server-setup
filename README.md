# Laravel Server Setup

## Description

A simple bash script to setup a Ubuntu server with Nginx, PHP 7.2 and MariaDB specifically for running Laravel applications.

### The script performs the following actions in this order:

1. Performs an `apt-get update` & `apt-get upgrade`
2. Installs and enables __Nginx__
3. Installs __PHP 7.2__ including other php packages required by Laravel
4. Installs and configures __MariaDB__
5. Installs __Composer__
6. Creates a `laravel` Nginx config file in sites-available and creates a sym link to it in sites-enabled 
7. Sets Laravel project directory permissions 
8. Performs a `composer install` inside your laravel project directory

## Installation

### Prerequisites

1. Have a freshly installed Ubuntu server
2. `git clone` your Laravel project directory somewhere onto the server. E.g. `/var/www/`

### Installing

First clone the `tdshaw/laravel-server-setup` repository onto your fresh Ubuntu server and navigate to the script:

```
cd ~
git clone https://github.com/tdshaw/laravel-server-setup.git
cd laravel-server-setup
```

Run the script and follow the prompts.

```
./laravel-server-setup
```

- - - -

Example usage:
```
$ ./laravel-server-setup

Enter laravel project directory (e.g. /var/www/laravel):
/var/www/laravel
Enter laravel server name (e.g. example.com). Leave blank if none:
example.com
Set mysql root password:
root
Enter mysql database name:
laravel_db
Enter mysql user name:
laravel_user
Enter mysql user password:
laravel_password
```

