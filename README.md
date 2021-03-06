# OVERVIEW [![License](https://img.shields.io/badge/License-GPL%20v3%2B-blue.svg?style=flat-square)](https://github.com/aanarchyy/FreeVPN/blob/master/LICENSE)

Tool to connect to FreeVPN
Put this script in the root of the folder of certs that you download from them.  Any arguments not specified will be asked.

# Requirements
Must have openvpn installed obviously.

# Usage

```
	Tool to connect to FreeVPN Version:0.4.2 (aanarchyy@gmail.com)
	./vpn-connect.sh {arguments}
	-u 	Server (se im it be co.uk me eu)
	-p 	Protocol (TCP UDP)
	-t 	Port (TCP-80/443 UDP-53/40000)
	-n 	Password to use
	-4 	Attempt to block IPV4 incase the VPN drops
	-6 	Attempt to block IPV6
	-r 	Restore old iptables rules if they are backed up
	-h 	help
```
**-u**
Select the server you wish to connect to.  Valid responses are:
1)me 2)se 3)im 4)it 5)be 6)co.uk 7)eu
Either the numbers or the actual address works.

**-p**
Protocol to use. Valid responses are either TCP or UDP.

**-t**
Port to use. Valid responses are if you use TCP, must use either 80 or 443, or UDP either 53 or 40000.

**-n**
Password to use. If not specified it will attempt to scrape it from the website.

**-4**
Add some iptables rules to attempt to halt traffic if the vpn drops the connection.

**-6**
Add some ip6tables rules to attempt to halt traffic for all IPV6.

**-r**
If you attempted to use either `-4-` or `-6`, your current iptables are backed up, this will attempt to restore what you had previous to running.
