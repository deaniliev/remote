![LaravelCollective Remote](LaravelCollectiveRemote-banner.png)

[![Build Status](https://travis-ci.org/LaravelCollective/remote.svg?branch=master)](https://travis-ci.org/LaravelCollective/remote)
[![Total Downloads](https://poser.pugx.org/LaravelCollective/remote/downloads)](https://packagist.org/packages/laravelcollective/remote)
[![Latest Stable Version](https://poser.pugx.org/LaravelCollective/remote/v/stable.svg)](https://packagist.org/packages/laravelcollective/remote)
[![Latest Unstable Version](https://poser.pugx.org/LaravelCollective/remote/v/unstable.svg)](https://packagist.org/packages/laravelcollective/remote)
[![License](https://poser.pugx.org/LaravelCollective/remote/license.svg)](https://packagist.org/packages/laravelcollective/remote)

Official documentation for Remote (SSH) for The Laravel Framework can be found at the [LaravelCollective](http://laravelcollective.com) website.

This repo is a fork of LaravelCollective's Remote.

# Installation

composer.json:

```
 "require": {
    ...
    "deanski/remote": "^6"
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
composer install
php artisan vendor:publish
```

# Usage

After connections are defined in confg/remote.php you can use SSH class directly:


SSH::run(['echo "This is a test"']);


