OwnCloud Bootswatch Themes
==========================

This is a collection of free themes for [Owncloud](http://owncloud.org/), based on [Bootswatch](http://bootswatch.com),
which is in turn based on [Bootstrap](http://getbootstrap.com/).

Usage
-----

Clone or download the repository, copy one of the themes to the `owncloud/themes` directory, and then
add `"theme" => "bootstrap_theme"` to `owncloud/config/config.php`, where `bootstrap_theme` is the name of the directory
you copied.

Head over to [Bootswatch](http://bootswatch.com) to take a look at the available themes. The default Bootstrap theme
is also included in this package, under `bootstrap`.

Customization
-------------

Just like Bootswatch, OwnCloud Bootswatch can be customized. Also like Bootswatch, OwnCloud Bootswatch uses Grunt and
NodeJS for building LESS files.

Working on top of Bootswatch patterns, the main file `global/owncloud.less` uses Bootstrap's `variables.less` file (and,
of course, Bootswatch's `variable.less` of each theme) to get the colors from Bootstrap and make some minor adjustments.

To modify a theme or create your own, follow the steps below in your terminal. You'll need to have Git and Node
installed.

    git clone https://github.com/rafaelgou/owncloud-bootswatch-themes
    npm install
    git submodule init
    git submodule update

Edit owncloud.less in one of the theme directories, or create your own in /custom. Please be aware that `global/owncloud`
is not a theme itself, but contains files used to build all themes - change it only if you want to change anything
globally.

Type `grunt swatch:[theme]` to build the CSS for a theme, e.g. `grunt swatch:amelia` for Amelia. `grunt swatch` by itself
builds all themes at once.

If you don't already have grunt available in the command line, install grunt-cli as described on the
[Grunt Getting Started page](http://gruntjs.com/getting-started).


Author
------

[Rafael Goulart](http://github.com/rafaelgou)

Contributors
------------

[Patrick Lavigne](https://github.com/PMLavigne)

Copyright and License
---------------------

Copyright 2014 Rafael Goulart

Bootstwatch Copyright 2015 Thomas Park

Code released under the MIT License.
