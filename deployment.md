# Deploy additional Postscreen daemon for ZCS 8.x

## Deployment Overview
* Backup the configuration file /opt/zimbra/postfix/conf/master.cf.in
* In the file master.cf.in, change the default port 25 to another TCP port (for example: 125) via your favorite editor
  * Note: See the configs file master.cf.in for more details
* Restart the Zimbra MTA service
  * Note: The Zimbra MTA service listened on port 125 assigned on loopback interface (127.0.0.1) or on other interfaces (depend on your scenario)
* Install a new Postfix service (not Zimbra Postfix)
* Backup two configs files of the new Postfix (main.cf & master.cf)
* Configure the new Postfix to use with the built-in Postscreen daemon
  * Note: See the configs files related to Postfix (postfix-main.cf, postfix-master.cf...) for more details
* Start the new Postfix service (via systemctl)
* Review your configs finally
* Test your deployment
