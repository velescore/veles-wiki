Name:               Veles OSX OpenVPN Guide
Image:              https://www.veles.network/images/download/mac-wallet.png
GuideType:          User's Guide
OS:                 Mac OSX
VelesdApp:          dVPN
Protocol:           OpenVPN
Requirements:       OpenVPN client
Difficulty:         Easy
EstimatedTime:      5 minutes

# OSX OpenVPN Guide 
This will guide you through the process of installing and using Tunnelblick on the OSX platform.  

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) **Install Tunnelblick Client**
2) **Download Veles OpenVPN config**

## Contents
* **Section A**: Download and Install Tunnelblick
* **Section B**: Configure Tunnelblick
* **Section C**: Connect to Veles d-VPN
* **Section D**: Test VPN Connection
***

### Section A: Download and Install Tunnelblick

***Step 1***  

* Tunnelblick is a free, open source OpenVPN client for Mac OS X. You can **download the latest disk image from the [Tunnelblick Downloads page](https://tunnelblick.net/downloads.html)**. Double-click the downloaded **.dmg** file and follow the prompts to install:  
[https://tunnelblick.net/downloads.html](https://tunnelblick.net/downloads.html)  

!!! tip "User Tip"
	Towards the end of the installation process, Tunnelblick will ask if you have any configuration files. It can be easier to answer **No** and let Tunnelblick finish. 

***

### Section B: Configure Tunnelblick

***Step 1***  

* After installing Tunnelblick, **download [Veles OpenVPN config file](https://explorer.veles.network/dapi/getOpenVPNConfig)**.  
https://explorer.veles.network/dapi/getOpenVPNConfig

***Step 2***  

* **Double-click veles.ovpn**. Tunnelblick will install the client profile.
  
!!! important "Important Note"
	Administrative privileges are required.  

***

### Section C: Connect to Veles d-VPN 

***Step 1***  

* Launch Tunnelblick by double-clicking **Tunnelblick** in the **Applications folder**.

!!! tip "User Tip"
	Once Tunnelblick has been launched, there will be a Tunnelblick icon in the menu bar at the top right of the screen for controlling connections.

***

***Step 2***  

* Click on the icon, and then the **Connect** menu item to initiate the VPN connection and select the **veles** connection.  

***

### Section D: Test VPN Connection

***Step 1***  

* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.

***

If you do, congratulations! You have now setup a Veles d-VPN . If you do not, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you.  
