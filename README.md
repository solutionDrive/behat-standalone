behat-standalone
================

Builds a phar containing a full behat installation that contains some other useful goodies.


Usage
-----

To create the phar, you need to install ```macfja/phar-builder``` globally,
for example by downloading the last release as a phar itself:

    curl -o createPhar -L `curl -s https://api.github.com/repos/MacFJA/PharBuilder/releases \
        | grep browser_download_url | head -n 1 | cut -d '"' -f 4`

Then you can just run the following command inside the repository:

    phar-builder.phar package


The newly created phar file can be used just like the ```behat``` binary is used:

    behat-standalone.phar --help


Thanks
------

Phar creation is inspired by:
https://andreas.heigl.org/2017/01/18/building-a-phar-automated/
