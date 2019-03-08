Symfony PHP CodeSniffer Coding Standard
========================================

A coding standard to check against the [Symfony coding standards](http://symfony.com/doc/current/contributing/code/standards.html), originally shamelessly copied from the -disappeared- opensky/Symfony2-coding-standard repository.

Installation
------------

### Composer
This standard can be installed with the [Composer](https://getcomposer.org/) dependency manager.

1. [Install Composer](https://getcomposer.org/doc/00-intro.md)

2. Install the coding standard as a dependency of your project

        composer require --dev anujith-singh/Symfony2-coding-standard

3. Check the installed coding standards for "Symfony"

        phpcs -i

4. Done!

        bin/phpcs --standard=Symfony2 /path/to/code


### Stand-alone

1. Install [PHP_CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer)

2. Checkout this repository 

        git clone git://github.com/anujith-singh/Symfony2-coding-standard.git

3. Move rules to squizlabs/PHP_CodeSniffer's Standards directory
        
        cp -R path/to/anujithsingh/symfony2-coding-standard/ vendor/squizlabs/php_codesniffer/src/Standards/Symfony2

4. Check the installed coding standards for "Symfony"

        phpcs -i

5. Done!

        phpcs --standard=Symfony2 /path/to/code


Contributing
------------

If you do contribute code to these sniffs, please make sure it conforms to the PEAR
coding standard and that the Symfony2-coding-standard unit tests still pass.

To check the coding standard, run from the Symfony2-coding-standard source root:

    $ phpcs --ignore=*/tests/* --standard=PEAR . -n

The unit-tests are run from within the PHP_CodeSniffer directory:

    $ phpunit --filter Symfony2_* tests/AllTests.php
