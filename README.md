ansible-nodejs for Debian/Ubuntu
============

Ansible role for installing Nodejs on Debian/Ubuntu linux systems.

## NodeSource and Chris Lea

Chris Lea is working with [NodeSource](https://nodesource.com/) to supply Ubuntu users with the latest stable NodeJS. This means the Launchpad PPA is not used anymore.

To help make this easy for users NodeSource and Chris Lea has provided a [shell script](https://deb.nodesource.com/setup) to install NodeJS. If you want to find out the reasoning behind the move, read [this post](https://chrislea.com/2014/07/09/joining-forces-nodesource/).

This Ansible role is a conversion of that shell script, making this role a mirror of the "semi official" way to install the latest stable NodeJS on Ubuntu.

## What it'll do?

This role mirrors the shell script, running the following tasks:

* Ensure the Ubuntu distro is supported. If it is supported, the remaining tasks are run:
* Remove the old Chris Lea NodeJS PPA, if it exists
* Add NodeSource GPG Keys
* Add NodeSource Apt Sources List
* Install NodeJS (including npm)
