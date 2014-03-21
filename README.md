Development environment
=======================

This will help you get set up with the Land Registry concept development environment.

Installation
------------

1. Check out this repository:

        $ git clone git@github.com:LandRegistry/development.git landregistry
        $ cd landregistry/

2. Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads) and [Vagrant](http://www.vagrantup.com/downloads.html).

3. Check out the other Land Registry repositories:

        $ script/bootstrap

Running stuff
-------------

Start the development VM:

    $ vagrant up

You can then log into the development VM:

    $ vagrant ssh

To run a service, change to its directory and run Fig:

    $ cd my-property/
    $ fig up

