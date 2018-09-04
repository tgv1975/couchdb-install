# couchdb-install
A straight-forward Bash script to install and configure CouchDB 2.2.0 on Ubuntu 18.04 Bionic Beaver 64-bit.

### What it does

* Upgrades apt and updates packages.
* Installs the official CouchDB **package**.
* Sets up CouchDB as a **service** that runs on system startup.
* Creates the "couchdb" system **user**.
* Checks CouchDB installation and attempts a **single node setup**.

### Usage
Download the couchdb-install file and run it:

`sudo ./couchdb-install`

or, with unnatended option enabled:

`sudo ./couchdb-install -y`

The script will guide you further.

Options (flags):

`-y`: Don't prompt for confirmation upon running the install.

### Compatibility
Tested on Ubuntu 18.04 Bionic Beaver 64-bit **only**, but it may work on other version of Debian-based systems.

### Acknowledgements
The script is based on information from the official docs and other sources:
* http://docs.couchdb.org/en/2.0.0/install/unix.html
* http://docs.couchdb.org/en/2.0.0/install/
* http://docs.couchdb.org/en/2.0.0/cluster/nodes.html
* https://www.jamescoyle.net/how-to/2527-add-systemd-startup-script-for-couchdb
* http://stackoverflow.com/a/40409701

### Issues
Error handling is not airtight. Some post-failure messages may not be very helpful.
