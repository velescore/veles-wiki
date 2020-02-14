Name:           Veles Windows Stunnel Guide
Image:          https://www.veles.network/images/download/windows-wallet.png
Date:           Feb 12 2020,
Version: 		1.01
Syntax:         Markdown
Authors:        @AltcoinBaggins @mdfkbtc

# Window Stunnel Guide
This explains the process of installing Stunnel as a client in Windows.

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) **Succesfully installed [[Windows OpenVPN Guide]]**  
2) **Install Stunnel**  
3) **Download Veles shieled OpenVPN config**  
4) **Download Veles Stunnel config**  

## Contents
* **Section A**: Download and Install Stunnel
* **Section B**: Configure Stunnel
* **Section C**: Connect Veles d-VPN with Stunnel
* **Section D**: Test VPN Connection
***

### Section A: Download and Install Stunnel

***Step 1***  

* Official Stunnel client application for Windows can be found on **[Stunnel’s Downloads page](https://www.stunnel.org/downloads.html)**. Choose the appropriate installer version for your version of Windows.  
[https://www.stunnel.org/downloads.html](https://www.stunnel.org/downloads.html)

!!! important "Important Note"
	Stunnel needs administrative privileges to install.

***

***Step 2***  

* In the end of install, it will open new console window. **You can input any information to these fields or let it blanc. It doesn’t matter and don’t have any affect to your connection**.

***

### Section B: Configure Stunnel

***Step 1***  

* After installing Stunnel, **download [Veles Stunnel configuration file](https://explorer.veles.network/dapi/getStunnelConfig) and [Shielded OpenVPN config](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)** from these URL's:  
[https://explorer.veles.network/dapi/getStunnelConfig](https://explorer.veles.network/dapi/getStunnelConfig)  
[https://explorer.veles.network/dapi/getShieldedOpenVPNConfig](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)  

***
  
***Step 2***  

!!! tip "User Tip"
	You will need rename veles.stunnel.conf to **stunnel.conf**

* Move downloaded Veles Stunnel config to it's repository:    
`C:\Program Files\Stunnel\config\`  
* Move downloaded Veles Shielded OpenVPN config to it's repository:    
`C:\Program Files\OpenVPN\config\`    

***

### Section C: Connect Veles d-VPN with Stunnel

***Step 1***  

* At first turn on Stunnel. Once Stunnel is started turn on OpenVPN client and initiate a connection by going into the system tray applet and right-clicking on the OpenVPN applet icon. This opens the context menu. Select **veles-shielded** at the top of the menu (that’s our veles-shielded.ovpn profile) and choose **Connect**.

!!! tip "User Tip"
	A status window will open showing the log output while the connection is established, and a message will show once the client is connected.  
	Disconnect from the VPN the same way: Go into the system tray applet, right-click the OpenVPN applet icon, select the client profile and click Disconnect.

***

### Section D: Test VPN Connection

***Step 1***  

* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.

***

If you do, congratulations! You have now setup a . If you do not, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you.  
