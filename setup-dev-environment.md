---
description: Contribute to Dopenote
---

# Setup dev environment

### Requirements

* PHP 7.3 \(_7.2 should work_\)
* Composer
* A mariadb/mysql server
* `npm` - to build javascript files

### Setup

1. Fork the repo on GitHub
2. Git clone your fork
3. Run `composer install` in the repo dir
4. Create a new database called `dopenote` \(collation: `utf8mb4_unicode_ci`\)
5. Rename the file `.env.example` to `.env`
6. Change the `DB_*` values in the `.env` file
7. Run `php artisan migrate:fresh`
8. Run `php artisan key:generate`
9. Run `php artisan serve`
10. Run `npm run dev` to build .js files \(or run `npm run watch`to watch for changes\)
11. See the site at [http://127.0.0.1:8000](http://127.0.0.1:8000/)

You can create an admin user by running `php artisan db:seed`- then you can login with email: `admin@localhost` and password: `12341234`

