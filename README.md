# Lumen Graphql Template/Boilerplate

The objective of this repo is build a graphql api boilerplate/template in lumen because at the time of building this project there was no attempt at github.

graphql is great, i use it on python and want to make it easier in php.


## How To Start / Setup

1 -  clone the repo with your api/project name

```shellscript
git clone https://github.com/marco-gallegos/lumen-graphql-template "your project name"
cd "your project name"
composer install
cp .env.example .env
```

2 - Nothing to do, serve and let's code. don't forget visit the /graphql-playground route



## Main Features

Some cool additional features in this template/boilerplate

### Laravel Generators (dev dependency)

Not supported by default in lumen, [a third party package](https://github.com/flipboxstudio/lumen-generator) that provides artisan commands like make:controller or serve

### Graphql Playground (dev dependency)

A sandbox for test your graphql api by [a third party package](https://github.com/mll-lab/laravel-graphql-playground).

Only need to acces to your development server on route /graphql-playground example http://localhost:8000/graphql-playground


### CORS

[Third party package](https://github.com/palanik/lumen-cors) preconfigured to add CORS headers to every request.

### JWT Auth

To Do

## Tips

Use [insomnia](https://insomnia.rest/) for test this project, if you use linux is available in snap store.

```shellscript
sudo snap install insomnia
```


## Configuration

### Graphql Server | [Lighthouse](https://lighthouse-php.com/)


steps to make lighthouse plugin works in lumen, inspired by [Bruno Silva on Medium](https://medium.com/@bsilva0x87/how-to-configure-laravel-lumen-with-lighthouse-php-graphql-ad63b8273321)

```shellscript
mkdir ./config

cp vendor/nuwave/lighthouse/config/config.php ./config/lighthouse.php

# checking lighthouse file created on schema -> register
# we need to replicate this file

mkdir ./graphql

cp vendor/nuwave/lighthouse/assets/default-schema.graphql ./graphql/schema.graphql

```

### Graphql Playground

```shellscript
cp vendor/mll-lab/laravel-graphql-playground/src/graphql-playground.php config/graphql-playground.php
```

```php
# adding this to app.php
/*
|--------------------------------------------------------------------------
| GraphQL Playground
|--------------------------------------------------------------------------
|
| Loads mll-lab/laravel-graphql-playground configuration file into the application.
|
*/
$app->configure('graphql-playground');
```

## License

The Lumen framework is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).
