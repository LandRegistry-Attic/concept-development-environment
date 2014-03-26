Development environment
=======================

This will help you get set up with the Land Registry concept development environment.

Installation
------------

1. Check out this repository:

        $ git clone git@github.com:LandRegistry/concept-development.git landregistry
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

    $ cd concept-my-property/
    $ fig up

The VM's IP address is 172.16.42.43 and all services will be available on that address. For example, concept-my-property can be accessed at [http://172.16.42.43:5000](http://172.16.42.43:5000). You might want to add a shortcut to your hosts file, e.g. [http://localdocker:5000](http://localdocker:5000).

