# Setup dev environment

### Requirements

* PHP 7.3
* Composer
* A mariadb/mysql server
* `npm` - if you need to change javascript files

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
10. See the site at [http://127.0.0.1:8000](http://127.0.0.1:8000/)
11. If you need to change any .js files, run `npm run dev` or `npm run watch`

