Name:               Veles OSX Stunnel Guide
Image:              https://www.veles.network/images/download/mac-wallet.png
GuideType:          User's Guide
OS:                 Mac OSX
VelesdApp:          dVPN
Protocol:           TLS/SSL (stunnel), OpenVPN
Requirements:       Stunnel, OpenVPN client
Difficulty:         Easy
EstimatedTime:      5 minutes

# OSX Stunnel Guide 
This will guide you through the process of installing and using Stunnel on the OSX platform.  

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) **Installed [[OSX OpenVPN Guide]]**  
2) **Install Stunnel**  
3) **Download Veles Shielded OpenVPN config**  
4) **Download Veles Stunnel config**  

## Contents
* **Section A**: Download and Install Stunnel
* **Section B**: Configure Stunnel
* **Section C**: Connect to Veles d-VPN with Stunnel
* **Section D**: Test VPN Connection
***

### Section A: Download and Install Stunnel 

***Step 1***  

* Press **Command+Space** and type **Terminal** and press enter/return key. Run in Terminal app and press enter/return key:  
`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" < /dev/null 2> /dev/null`  

!!! important "Important Note"
	Administrative privileges are required.

***

***Step 2***  

* After previous command finish **install Stunnel** by typing :  
`brew install stunnel`  

***

### Section B: Configure Stunnel

***Step 1***  

* **Download [Veles Stunnel configuration file](https://explorer.veles.network/dapi/getStunnelConfig)**:   
[https://explorer.veles.network/dapi/getStunnelConfig](https://explorer.veles.network/dapi/getStunnelConfig)  

***

***Step 2***  

* **Move downloaded Veles Stunnel config to it's repository**:  
`/usr/local/etc/stunnel/`  
  
!!! tip "User Tip"
	You will need rename veles.stunnel.conf to stunnel.conf.

***

***Step 3***  

* **Download [Veles Shielded OpenVPN config](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)**:   
[https://explorer.veles.network/dapi/getShieldedOpenVPNConfig](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig) 

***

***Step 4***  

* Tunnelblick will **install Veles Shielded OpenVPN** profile by doubleclicking on **veles-shielded.ovpn**.  

!!! important "Important Note"
	Administrative privileges are required.

***

### Section C: Connect to Veles d-VPN with Stunnel

***Step 1***  

* Press **Command+Space** and type **Terminal** and press **enter/return** key. Now we will turn on Stunnel by typing :  
`stunnel`

***

***Step 2***  

* Now launch **Tunnelblick** by double-clicking Tunnelblick in the Applications folder.

***

***Step 3***  

* Once Tunnelblick has been launched, there will be a Tunnelblick icon in the menu bar at the top right of the screen for controlling connections. Click on the icon, and then the Connect menu item to initiate the VPN connection. Select the **veles-shielded** connection.

***

### Section D: Test VPN Connection

***Step 1***  

* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.

***

If you do, congratulations! You have now setup a Veles d-VPN . If you do not, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you.  
