## Laravel 4 with Sentry 2 - Version 2.0
This is a fork of [L4withSentry](https://github.com/rydurham/L4withSentry) upgraded to Laravel 4.2 with full support for Mailgun/Mandrill driver methods of sending email (added Guzzle to composer), and with Codesleeve Asset Pipeline fully integrated as well.

This is a demo of [Sentry 2](https://github.com/cartalyst/sentry) integrated with [Laravel 4](https://github.com/laravel/laravel/tree/develop) and [Bootstrap 3.0](http://getbootstrap.com).  This repo is intended to be for reference only - if you want to use this code in your own app I suggest using [Sentinel](https://github.com/rydurham/Sentinel) - a laravel pacakge based on this repo.  

### Instructions

Before you begin, make sure you have both ```git``` and ```composer``` installed on your system. 

1. Clone the repo
2. Run ```php composer.phar update```
3. Set up your datbase configuration in ```app/config/database.php```
4. Edit ```app/config/mail.php``` to work with your mail setup.
5. Run the migrations: ```php artisan migrate```
6. Seed the Database: ```php artisan db:seed```
7. For asset-pipeline to work edit ```bootstrap/start.php```

	$env = $app->detectEnvironment(array(
    	'local' => array('your-machine-name'),
  	));

### Database
The Default DB is setup to use SQLite for testing as its the fastest way to get a testapp up and running.

### Seeds
The seeds in this repo will create two groups and two user accounts.

__Groups__
* Users
* Admins

__Users__
* user@user.com  *Password: sentryuser*
* admin@admin.com *Password: sentryadmin*

### Links
* [Sentry 2.0 Documentation](https://cartalyst.com/manual/sentry)
* [Laravel 4 Documentation](http://laravel.com/docs)
* [Laravel: From Apprentice To Artisan](https://leanpub.com/laravel) by Taylor Otwell
* [Implementing Laravel](https://leanpub.com/implementinglaravel) by Chris Fidao
* [Laracasts](http://laracasts.com)

### Tests
[![Build Status](https://travis-ci.org/rydurham/L4withSentry.svg?branch=master)](https://travis-ci.org/rydurham/L4withSentry)

1. Make sure you've run `composer update`.
2. cd to the L4withSentry project root directory.
3. Execute `phpunit` to run tests or `phpunit --coverage-text` to see text based code coverage summary.

### Notes
* Tests are currently very limited.  

### History
Version 2.0 has been completely revamped using strategies suggested in *Laravel: From Apprentice to Artisan* by Taylor Otwell, *Implementing Laravel* by Chris Fidao and the Laracast videos.   Version 1.0 still exists in its original version. 

=======
The Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT)
