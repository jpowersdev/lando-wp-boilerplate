# Lando WordPress Boilerplate

Run this shell script and have a WordPress site up in seconds.

## Requirements

- Lando - [Install](https://docs.lando.dev/basics/installation.html)

## Usage

`git clone git@github.com:jpowersdev/lando-wp-boilerplate my-site`
`cd my-site && ./setup`

## What it Does

- Downloads latest version of WordPress
- Spins up container including PhpMyAdmin and Mailhog
- Creates `wp-config.php`
- Installs WordPress with reasonable defaults 
    - Site name pulled from `.lando.yml`
    - `admin` and `password` because it's local
- Deletes setup script and git files, leaving you with a clean project

## Customizing

*Must be done before running the `start` script*

- Change the `name` property in `.lando.yml` for each new project to avoid collisions.
- Change the variables passed to `wp core install` in the `wp-import` tooling to change credentials.