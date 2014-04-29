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
    
Before the first time you run the development environment, you need to run a script to set up the geo database:

    $ script/setup-geodb

To run the whole development environment, run Fig:

    $ fig up

A few useful places to start:

 - [View properties](http://172.16.42.43:8001)
 - [Add properties](http://172.16.42.43:8002)

The VM's IP address is 172.16.42.43 and all services will be available on that address. For example, properties can be accessed at [http://172.16.42.43:8001](http://172.16.42.43:8001). You might want to add a shortcut to your hosts file, e.g. [http://localdocker:8001](http://localdocker:8001).

Loading test data
-----------------

If you want to load some test data, run this script (it'll take a while, but you can exit half way through if you only want a partial data set):

    $ script/populate-with-data

Setting up a new project
------------------------

 - Add to `script/bootstrap`, `.gitignore` and `fig.yml` in this repo
 - Add to [Fourth Wall config](https://gist.github.com/bfirsh/71618c20c941c3e7e9cd)
 - Travis
 - Heroku
 - Slack integration on master branch only

