codeception_project
===================

###  Codeception : 

Codeception PHP Testing Framework is designed to work just out of the box. This means its installation requires minimal steps and no external dependencies preinstalled (except PHP, of course). Only one configuration step should be taken and you are ready to test your web application from an eye of actual user. 

### Requrement :


PHP version minimum 5.4

PHP Composer component

### Installation :

1. Open you terminal

2. Go to /var/www/html/ & create a directory , I create a directory name as codecept_project"

3. Create a composer.json file & past the folling contain.. 

```javascript
	{
		"require" :{
		},
		"require-dev": {
			"codeception/codeception": "2.0.8"
		}
	}
```

4.  Go to your created directory 
```sh
	$ cd /var/www/html/codecept_project/
	$ composer install --dev
```


5. You can see a directory has been created name like "vendor", then run the following command
```sh
	$ php codecept.phar bootstrap
```
6.  Generate your first acceptance test. Acceptance tests emulate behavior of a real user visiting your site.
```sh

	$ php codecept.phar generate:cept acceptance Welcome
```
7.  Configure Acceptance Tests 

   Please make sure your local dev serveris running.  Put application URL into:  tests/acceptance.suite.yml 
```javascript
	class_name: AcceptanceGuy 
		modules: 
		enabled: [PhpBrowser, AcceptanceHelper]
		config: 
  			PhpBrowser:
      			url: '{YOUR APP'S URL}'

```
8.  Run 
```sh
	php codecept.phar run
```
9.  If you did everything right and your app has "Home" text on frontpage you will see this in output 
```javascript
	Suite acceptance started 
	Trying to ensure that frontpage works (WelcomeCept.php) - Ok
	Suite functional started
	Suite unit started

	Time: 1 second, Memory: 21.00Mb
	OK (1 test, 1 assertions)
```
That's it.


	

