## Deploy to Bluemix Yii 2 Basic Project Template

### Step 1 clone the code and setup

Open your terminal
```
$ git clone https://github.com/Twanawebtech/yii2App-Bluemix.git
$ cd yii2App
```
Open the manifest.yml file and change the name and host to the app name you want to call it.
Name and Host must be a unique name that was not taken before, if you selected a name that already been used then you should get error message in your terminal.

Now, with that you are ready to push your app to Bluemix.
- Given that you already have installed the cloud Foundry CLI, if you haven't there do that first.


### Step 2 Deploy your code to Bluemix

Connect to IBM Bluemix
```
$ bluemix api https://api.ng.bluemix.net
bluemix login -u <your bluemix email id> -o "<your bluemix email id>" -s "<your space>"
```

Login to Bluemix
```
$ bluemix api https://api.ng.bluemix.net
bluemix login -u <your bluemix email id> -o "<your bluemix email id>" -s "<your space>"
```

Deploy your app to Bluemix
```
$ bluemix api https://api.ng.bluemix.net
bluemix login -u <your bluemix email id> -o "<your bluemix email id>" -s "<your space>"
```

Push your code to Bluemix
```
$ cf push phpinfo-jbs2 -b https://github.com/cloudfoundry/php-buildpack.git -s cflinuxfs2
```


Access your app by entering the following URL into your browser:
<your-app-name>.mybluemix.net/yii

*Note, this is running the main "Yii 2 with basic application template" for path fixes, refer to the (link here)[http://www.yiiframework.com/download/]*

Done!



-----

Yii 2 Basic Project Template
============================

Yii 2 Basic Project Template is a skeleton [Yii 2](http://www.yiiframework.com/) application best for
rapidly creating small projects.

The template contains the basic features including user login/logout and a contact page.
It includes all commonly used configurations that would allow you to focus on adding new
features to your application.

[![Latest Stable Version](https://poser.pugx.org/yiisoft/yii2-app-basic/v/stable.png)](https://packagist.org/packages/yiisoft/yii2-app-basic)
[![Total Downloads](https://poser.pugx.org/yiisoft/yii2-app-basic/downloads.png)](https://packagist.org/packages/yiisoft/yii2-app-basic)
[![Build Status](https://travis-ci.org/yiisoft/yii2-app-basic.svg?branch=master)](https://travis-ci.org/yiisoft/yii2-app-basic)

DIRECTORY STRUCTURE
-------------------

      assets/             contains assets definition
      commands/           contains console commands (controllers)
      config/             contains application configurations
      controllers/        contains Web controller classes
      mail/               contains view files for e-mails
      models/             contains model classes
      runtime/            contains files generated during runtime
      tests/              contains various tests for the basic application
      vendor/             contains dependent 3rd-party packages
      views/              contains view files for the Web application
      web/                contains the entry script and Web resources



REQUIREMENTS
------------

The minimum requirement by this project template that your Web server supports PHP 5.4.0.


INSTALLATION
------------

### Install from an Archive File

Extract the archive file downloaded from [yiiframework.com](http://www.yiiframework.com/download/) to
a directory named `basic` that is directly under the Web root.

Set cookie validation key in `config/web.php` file to some random secret string:

```php
'request' => [
    // !!! insert a secret key in the following (if it is empty) - this is required by cookie validation
    'cookieValidationKey' => '<secret random string goes here>',
],
```

You can then access the application through the following URL:

~~~
http://localhost/basic/web/
~~~


### Install via Composer

If you do not have [Composer](http://getcomposer.org/), you may install it by following the instructions
at [getcomposer.org](http://getcomposer.org/doc/00-intro.md#installation-nix).

You can then install this project template using the following command:

~~~
php composer.phar global require "fxp/composer-asset-plugin:~1.1.1"
php composer.phar create-project --prefer-dist --stability=dev yiisoft/yii2-app-basic basic
~~~

Now you should be able to access the application through the following URL, assuming `basic` is the directory
directly under the Web root.

~~~
http://localhost/basic/web/
~~~


CONFIGURATION
-------------

### Database

Edit the file `config/db.php` with real data, for example:

```php
return [
    'class' => 'yii\db\Connection',
    'dsn' => 'mysql:host=localhost;dbname=yii2basic',
    'username' => 'root',
    'password' => '1234',
    'charset' => 'utf8',
];
```

**NOTES:**
- Yii won't create the database for you, this has to be done manually before you can access it.
- Check and edit the other files in the `config/` directory to customize your application as required.
- Refer to the README in the `tests` directory for information specific to basic application tests.
