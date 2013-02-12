Customized Nette Framework Sandbox
=======================

The basic skeleton of application.

Customizations
--------------

### Third party components (installed by Composer if possible)

#### Backend components
+ [Webloader](https://github.com/janmarek/WebLoader)
+ [BootstrapFormRenderer](https://github.com/Kdyby/BootstrapFormRenderer)

#### Frontend components
+ [Twitter bootstrap](https://github.com/twitter/bootstrap)
+ [Font Awesome](https://github.com/FortAwesome/Font-Awesome)
+ [Nette Ajax](https://github.com/vojtech-dobes/nette.ajax.js)


### Other components

+ [SendmailMailer](https://github.com/lovec/my-nette-sandbox/blob/master/libs/Local/SendmailMailer.php) For sending emails in development only on demand
+ [ModelLoader](http://pla.nette.org/cs/nacitani-modelu-s-notorm-a-dependency-injection) For loading models. Needs review to DI
+ [Changelog module](https://github.com/lovec/my-nette-sandbox/tree/master/app/modules/ChangelogModule) For handling changes in db structure see readme for installation instructions

What is [Nette Framework](http://nette.org)?
------------------------

Nette Framework is a popular tool for PHP web development. It is designed to be
the most usable and friendliest as possible. It focuses on security and
performance and is definitely one of the safest PHP frameworks.

Nette Framework speaks your language and helps you to easily build better websites.


Installing
----------

The best way to install Nette Framework is to download latest package
from http://nette.org/download or create new project using
[Composer](http://doc.nette.org/composer):

	curl -s http://getcomposer.org/installer | php
	php composer.phar create-project nette/sandbox myApp dev-release-2.0.x
	cd myApp

Make directories `temp` and `log` writable. Navigate your browser
to the `www` directory and you will see a welcome page. PHP 5.4 allows
you run `php -S localhost:8888 -t www` to start the webserver and
then visit `http://localhost:8888` in your browser.


It is CRITICAL that file `app/config/config.neon` & whole `app`, `log`
and `temp` directory are NOT accessible directly via a web browser! If you
don't protect this directory from direct web access, anybody will be able to see
your sensitive data. See [security warning](http://nette.org/security-warning).
