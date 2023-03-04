## Laravel Boilerplate
* PHP 8.2.3
* Laravel 10.2.0
* MySQL 8.0
* Nginx 1.23.3

1) After cloning repo put environmental variables into **.env** (you need to create this file) as in **.env.example**
2) `docker compose up -d` to build and run up containers
3) After installation check permissions on **var** folder where your MySQL container installed. They should be as your `UID` user and `GID` usergroup.
If they are not, just enter `sudo chown -R YOURUSER:YOURGROUP var` outside the PHP container
4) Get into PHP container running command `docker compose exec php bash`
5) To install Composer dependencies run `composer install && composer dump-autoload` in the PHP container
6) Check the `/` route if it's working and shows you Laravel greeting page
7) Enjoy and develop!