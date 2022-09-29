

Official documentation for Remote (SSH) for The Laravel Framework can be found at the [LaravelCollective](http://laravelcollective.com) website.

This repo is a fork of LaravelCollective's Remote.

Added Laravel 9 support and install howto.

# Installation

composer.json:

```
 "require": {
    ...
    "deaniliev/remote": "^6"
 },
```

config/app.php:

```
'providers' => [

  Collective\Remote\RemoteServiceProvider::class,
]

'aliases' => Facade::defaultAliases()->merge([
        // 'ExampleClass' => App\Example\ExampleClass::class,
        'SSH' => \Collective\Remote\RemoteFacade::class,
])->toArray(),

```

```
composer update
php artisan vendor:publish
```

# Usage

After connections are defined in confg/remote.php you can use SSH class directly:


SSH::run(['echo "This is a test"']);


