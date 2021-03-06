# c9-lemp

This repo holds all the script, config files and commands that you might want to
use to set up a LEMP environment using MYSQL5.7, NGINX and PHP7.1-FPM instead the default
Apache2 runner for PHP applications and MYSQL5.5 on Cloud9 workspaces.

### Prerequisite

Setup a c9 workspace using the Apache, PHP5 and MySQL template

Upgrade MySQL 5.5 to 5.6 and finally to 5.7, using this:
``` bash
wget https://github.com/venom1724/c9-lemp/blob/master/mysql-apt-config_0.8.7-1_all.deb
sudo dpkg -i mysql-apt-config_0.8.7-1_all.deb
```
Choose MySQL 5.6, then
``` bash
sudo apt-get update
sudo apt-get install mysql-server
sudo dpkg-reconfigure mysql-apt-config
```
Now choose MySQL 5.7, then
``` bash
sudo apt-get update
sudo apt-get install mysql-server
```

### Usage

Run any of this commands straightaway on your c9 terminal.

``` bash
curl -L https://raw.githubusercontent.com/venom1724/c9-lemp/master/install.sh | bash
```
----
``` bash
wget -O - https://raw.githubusercontent.com/venom1724/c9-lemp/master/install.sh | bash
```

After completing this process your environment will also be provisioned with a
simple command to start, stop and restart the whole stack in a brief:

* `lemp start` // Starts NGINX and PHP and MySql
* `lemp stop`
* `lemp restart`
* `lemp status`

### Updating

You can re-run this script as many times as you wish, just in case something is updated.


### Considerations

This is a quite simple script. It is just an easy way to configure your environment
to be up and running with NGINX and PHP-FPM.

It does not override the default NGINX site configuration file, so you don't have to
worry about loosing any data in case you had already modified yours.
