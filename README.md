# Zimbra-Postscreen
## Project Overview
Sharing key notes & technical guides to deploy additional Postscreen daemon for ZCS 8.x (open source edition).

## Why Postscreen?
* Keeping the zombies/spambots away
* By keeping the zombies/spambots away, Postscreen leaves more SMTP server processes available for legitimate clients, 
and delays the onset of server overload conditions

## A brief introduction to Postscreen
* Postscreen is a daemon integrated in Postfix since version 2.8 and later
* The Postfix postscreen daemon provides additional protection against mail server overload
* For more details, go to the main page of Postscreen: http://www.postfix.org/POSTSCREEN_README.html

## Scenario without/with Postscreen
* Scenario in this project (anti-spam for Inbound SMTP traffic):
  Internet message(s) -> Postfix (running Postscreen) -> Zimbra Postfix (running built-in anti-spam/virus) -> Zimbra Mailbox
* Scenario in general: https://wiki.zimbra.com/wiki/Zimbra_Collaboration_Postscreen

## Requirements for Testing Environment
* OS: CentOS 7.x, 64-bit
* Software:
  * Zimbra: 8.6, 64-bit
  * Postfix (not Zimbra Postfix): 2.10, 64-bit

## Requirements for Production Environment
* OS: CentOS 6.x or 7.x, 64-bit
* Software:
  * Zimbra: 8.x, 64-bit
  * Postfix (not Zimbra Postfix): >=2.8, 64-bit (recommended version: >=2.10)

## Notes
* Postscreen daemon will be enabled in ZCS 8.7 by default
* In ZCS 8.6 and lower version, you have to build another Postscreen daemon running on same Zimbra MTA host
or running on a separate host (Postfix)

## License
See the license file "LICENSE" for more details.
