# Zimbra-Postscreen
## Project Overview
Sharing key notes to setup additional Postscreen daemon for ZCS 8.6 (open source edition).

## Why Postscreen?
* Keeping the zombies/spambots away
* By keeping the zombies/spambots away, Postscreen leaves more SMTP server processes available for legitimate clients, 
and delays the onset of server overload conditions

## A brief introduction to Postscreen
* Postscreen is a daemon integrated in Postfix since version 2.8 and later
* The Postfix postscreen daemon provides additional protection against mail server overload
* For more details, go to the main page of Postscreen: http://www.postfix.org/POSTSCREEN_README.html

## Scenario without/with Postscreen
* https://wiki.zimbra.com/wiki/Zimbra_Collaboration_Postscreen

## Environment For Testing Postscreen
* OS: CentOS 7.x, 64-bit
* Software:
  * Zimbra: 8.6, 64-bit
  * Postfix (not Zimbra Postfix): >=2.10, 64-bit
