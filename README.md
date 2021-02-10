# Torrent Box Tutorial

### Getting Started:

---

**Rasberry Pi 2/3/4**
*This tutorial assumes you've already:*

* Gained a basic understanding of working with the Linux command line.

* Installed the latest version of [Raspberry Pi OS Lite](https://downloads.raspberrypi.org/raspios_lite_armhf/images/raspios_lite_armhf-2021-01-12/2021-01-11-raspios-buster-armhf-lite.zip), run the `raspi-config` command, and established a working connection to the internet.)*

* Paid for a VPN subscription that will help maintain your privacy.

If you still need a VPN subscription, I'd highly recommened [PrivateInternetAccess.com](http://www.privateinternetaccess.com/pages/buy-a-vpn/1218buyavpn?invite=U2FsdGVkX1-MyKjtJ2elxr-u_Z7E7ZVXuIBDNEY55Ww%2CcTAHlCvPgR3Ct2n3lq3W1M0FF5E). Their prices are very affordable.

*(**Full Disclosure:** The link above is my personal referral link for PrivateInternetAccess.com.)*

### Step-by-Step:
---
1. **Install Prerequisites**
	1. Use apt *(or **apt-get**)* to install **OpenVPN**, **Transmission**, **unzip**, **curl**, and **Firefox**.
	
	```
	sudo apt update && sudo apt install openvpn transmission-daemon unzip curl firefox-esr -y
	```

---
	
2. **Configure Transmission**

	1. Stop Transmission
	
	```
	sudo systemctl stop transmission-daemon.service
	```

	2. Backup the original config file

	```
	sudo cp /etc/transmission-daemon/settings.json /etc/transmission-daemon/settings.json.bak
	```

	3. Create directory for downloads.

	```
	sudo mkdir /mnt/downloads
	```
	
	4. Alter the following settings in `/etc/transmission-daemon/settings.json`

		1. Set `"download-dir": "/var/lib/transmission-daemon/downloads"` to `"download-dir": "/mnt/downloads"`

		2. Add your local network IP address - or any other wildcard values - you might want to use to the `rpc-whitelist` values, separated by commas. *(Common examples of wildcards for a LAN would be **192.168.\*.\*** or **10.0.0.\***.)*

		3. `"rpc-password": "PASSWORD"`... Replace everything between the quotes with your password.

		4. Change username in `"rpc-username": "USERNAME"` to whatever username you want to use. *(This **does not** have to be your computer username.)*
		
		5. Save your changes and exit.

---

3. **Configure OpenVPN**

	1. Download the [OpenVPN configuration files](https://www.privateinternetaccess.com/openvpn/openvpn.zip) from your VPN service provider. **(Use `wget` to download the zip file.)**
	
	```
	wget https://www.privateinternetaccess.com/openvpn/openvpn.zip
	```
	
	2. Unzip the the file.
	
	```
	unzip openvpn.zip
	```
	
	3. Copy your preferred **.ovpn** configuration file to the `/etc/openvpn` directory as `default.conf`. *(I chose one close to my home in Northern California.)*
	
	```
	sudo cp us_silicon_valley.ovpn /etc/openvpn/default.conf
	```
	
	4. Create a file to store your VPN credentials *(ie. username and password)* by running `sudo nano /etc/openvpn/.creds`.
	
	**Example:**
	```
	user
	password
	```

---

4. 

5. 

6. 

7. 

8. 

9. 

10.
