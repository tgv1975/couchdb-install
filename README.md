# couchdb-install
A straight-forward Bash script to install and configure CouchDB 2.x on Ubuntu 16.04 Xenial Xerus 64-bit.

### What it does

* Upgrades apt and updates packages.
* Installs CouchDB **dependencies**.
* **Installs CouchDB** in `/home/couchdb`, by downloading the official source, and then building it.
* Sets up CouchDB as a **service** that runs on system startup.
* Creates the "couchdb" system **user**.
* Checks CouchDB installation and attempts a **single node setup**.
* Assists in creating the first CouchDB admin user, thus neutralizing the Admin Party.

### Usage
Download the couchdb-install file and run it:

`sudo ./couchdb-install`

or, with both options enabled,

`sudo ./couchdb-install -y -upgrade-system`

The script will guide you further.

Options (flags):

`-y`: Don't prompt for confirmation upon running the install (see Warning below).
`-upgrade-system`: The script will run `apt-get upgrade` and `apt-get update` prior to actually installing CouchDB. Updating the system is highly recommended before using the installer, because missing tools and dependencies will cause it to fail.


### Warning
The script installs CouchDB in `/home/couchdb`, **overwriting everything** in that directory!
If you've used this script to install CouchDB in the past, you may wish to save your settings and data before running this install.

### Compatibility
Tested on Ubuntu Xenial Xerus 64-bit **only**, but it should work on other version of Debian-based systems.

### Acknowledgements
The script is based on information from the official docs and other sources:
* http://docs.couchdb.org/en/2.0.0/install/unix.html
* http://docs.couchdb.org/en/2.0.0/install/
* http://docs.couchdb.org/en/2.0.0/cluster/nodes.html
* https://www.jamescoyle.net/how-to/2527-add-systemd-startup-script-for-couchdb
* http://stackoverflow.com/a/40409701

### Issues
Error handling is not airtight. Some post-failure messages may not be very helpful.

