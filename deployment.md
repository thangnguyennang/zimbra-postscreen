# Setup additional Postscreen daemon for ZCS 8.6

## Deployment Overview
* Backup the configuration file /opt/zimbra/postfix/conf/master.cf.in
* In the file master.cf.in, change the default port 25 to another TCP port (for example: 125)
via your favorite editor
  * Note: See the configs file master.cf.in for more details
* Restart the Zimbra MTA service
  * Note: After restarting, the Zimbra MTA service listened on port 125 on loopback interface
* Install a new Postfix service (not Zimbra Postfix)
* Backup two configs files of the new Postfix (main.cf & master.cf)
* Start the new Postfix service (via systemctl)
* Configure the new Postfix service to use the built-in Postscreen daemon
