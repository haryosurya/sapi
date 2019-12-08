API tester for laravel-admin
============================

## Installation

```
$ composer require laravel-admin-ext/api-tester -vvv

$ php artisan vendor:publish --tag=api-tester

```

Then last run flowing command to import menu and permission: 

```
$ php artisan admin:import api-tester
```

Finally open `http://localhost/admin/api-tester`.

## Configuration

`api-tester` supports 3 configuration, open `config/admin.php` find `extensions`:
```php

    'extensions' => [
    
        'api-tester' => [
        
            // route prefix for APIs
            'prefix' => 'api',

            // auth guard for api
            'guard'  => 'api',

            // If you are not using the default user model as the authentication model, set it up
            'user_retriever' => function ($id) {
                return \App\User::find($id);
            },
        ]
    ]

```
