behat-standalone
================

Builds a phar containing a full behat installation that contains some other useful goodies.


Usage
-----

To create the phar, you need to install ```kherge/box``` globally:
(The global composer bin path needs to be available in $PATH)

    composer global require kherge/box

Install the dependencies

    composer install --optimize-autoloader -n

Create the phar file

    box build -c box.json
    
Perhaps it is necessary to allow php to create a phar

    php -d phar.readonly=0 ~/.composer/vendor/bin/box build -c box.json

The newly created phar file can be used just like the ```behat``` binary is used:

    behat-standalone.phar --help


Thanks
------

Phar creation is inspired by:
https://andreas.heigl.org/2017/01/18/building-a-phar-automated/
