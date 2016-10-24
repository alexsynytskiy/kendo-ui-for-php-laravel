# Laravel Package

This package provides you with a simple tool to set up Kendo UI into your project

## Installation

In project composer.json

    "require": {
	    "synytskiy/laravel-kendo-ui": "dev-master"
	},
    "repositories": [
	  {
		"type": "vcs",
		"url": "git@github.com:alexsynytskiy/kendo-ui-for-php-laravel.git"
	  }
	]
    
After that from application directory in terminal:
    php composer.phar update
    
When package downloaded, add the service provider in `config/app.php` at the end of "providers" array:

    'Kendo\KendoUIServiceProvider',
    
And as last run command in terminal to copy assets from package into "public" directory:

    php artisan vendor:publish --tag=public --force

## Usage

Including of assets:

    src="{{ asset('vendor/synytskiy/js/jquery.min.js') }}"
    
Classes usage:

    $errorBars = new \Kendo\Dataviz\UI\ChartSeriesItemErrorBars();
