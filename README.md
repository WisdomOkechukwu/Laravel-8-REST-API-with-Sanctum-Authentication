<p align="center"><a href="https://laravel.com" target="_blank"><img src="https://raw.githubusercontent.com/laravel/art/master/logo-lockup/5%20SVG/2%20CMYK/1%20Full%20Color/laravel-logolockup-cmyk-red.svg" width="400"></a></p>

<p align="center">
<a href="https://travis-ci.org/laravel/framework"><img src="https://travis-ci.org/laravel/framework.svg" alt="Build Status"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/dt/laravel/framework" alt="Total Downloads"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/v/laravel/framework" alt="Latest Stable Version"></a>
<a href="https://packagist.org/packages/laravel/framework"><img src="https://img.shields.io/packagist/l/laravel/framework" alt="License"></a>
</p>
# Laravel REST API with Sanctum

This is an example of a REST API using auth tokens with Laravel Sanctum

## Usage

Change the *.env.example* to *.env* and add your database info

For MYSQL
```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=api
DB_USERNAME=root
DB_PASSWORD=
```

Create a MYSQL database and serve
(Use POstman to verify show the output)
```
php artisan serve
```

## Routes

```
# Public

GET   /api/products
GET   /api/products/:id

POST   /api/login
@body: email, password

POST   /api/register
@body: name, email, password, password_confirmation


# Protected

POST   /api/products
@body: name, slug, description, price

PUT   /api/products/:id
@body: ?name, ?slug, ?description, ?price

DELETE  /api/products/:id

POST    /api/logout
```
