# Torrent Box Tutorial

### Prerequisites:
---
**Rasberry Pi 2/3/4**
*This tutorial assumes you've already:*

* Installed the latest version of Raspberry Pi OS, run the `raspi-config` command, and established a working connection to the internet.)*

* Paid for a VPN subscription that will help maintain your privacy.

If you still need a VPN subscription, I'd highly recommened [PrivateInternetAccess.com](http://www.privateinternetaccess.com/pages/buy-a-vpn/1218buyavpn?invite=U2FsdGVkX1-MyKjtJ2elxr-u_Z7E7ZVXuIBDNEY55Ww%2CcTAHlCvPgR3Ct2n3lq3W1M0FF5E). Their prices are very affordable.

*(**Full Disclosure:** The link above is my personal referral link for PrivateInternetAccess.com.)*

### Step-by-Step:
---
1. Install OpenVPN & Transmission-Daemon
	1. `sudo apt update && sudo apt install openvpn transmission-daemon -y`
	
2. Configure Transmission
	1. Stop Transmission
		`sudo systemctl stop transmission-daemon.service`
	2. Backup the original config file
		`sudo cp /etc/transmission-daemon/settings.json /etc/transmission-daemon/settings.json.bak`
	3. Alter the following settings in `/etc/transmission-daemon/settings.json`
		1. ``
		2. ``
		3. ``
		4. ``
		5. ``

3. 

4. 

5. 

6. 

7. 

8. 

9. 

10.
