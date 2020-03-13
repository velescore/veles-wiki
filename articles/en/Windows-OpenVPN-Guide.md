Name:               Veles Windows OpenVPN Guide
Image:              https://www.veles.network/images/download/windows-wallet.png
GuideType:          User's Guide
OS:                 Windows
VelesdApp:          dVPN
Protocol:           OpenVPN
Requirements:       OpenVPN client
Difficulty:         Easy
EstimatedTime:      5 minutes

# Windows OpenVPN Guide 
This will guide you through the process of installing and using OpenVPN on the Windows platform.  

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) **Install OpenVPN Client**  
2) **Download Veles OpenVPN config**  

## Contents
* **Section A**: Download and Install OpenVPN
* **Section B**: Configure OpenVPN
* **Section C**: Connect to Veles d-VPN
* **Section D**: Test VPN Connection
***

### Section A: Download and Install OpenVPN

***Step 1***  

* The OpenVPN client application for Windows can be found on **[OpenVPN’s Downloads page](https://openvpn.net/community-downloads/)**. Choose the appropriate installer version for your version of Windows.  
[https://openvpn.net/community-downloads/](https://openvpn.net/community-downloads/)

!!! important "Important Note"
	OpenVPN needs administrative privileges to install.
 
***

### Section B: Configure OpenVPN

***Step 1***  

* After installing OpenVPN, **download [Veles OpenVPN config file](https://explorer.veles.network/dapi/getOpenVPNConfig)**.  
[https://explorer.veles.network/dapi/getOpenVPNConfig](https://explorer.veles.network/dapi/getOpenVPNConfig)

***

***Step 2***  

* Copy the **veles.ovpn** config file to:  
`C:\Program Files\OpenVPN\config`

***

***Step 3***  

* Now **launch OpenVPN**, it will automatically see the profile and makes it available.

!!! tip "User Tip"
	OpenVPN must be **run as an administrator** each time it’s used, even by administrative accounts. To do this without having to right-click and select Run as administrator every time you use the VPN, you can preset this, but this must be done from an administrative account.    
	To set the OpenVPN application to **always run as an administrator, right-click on its shortcut icon** and go to **Properties**. At the bottom of the **Compatibility tab**, click the button to Change settings for all users. In the new window, **check Run this program as an administrator**.

***

### Section C: Connect to Veles d-VPN 

***Step 1***  

* Once OpenVPN is started, initiate a connection by going into the system tray applet and right-clicking on the OpenVPN applet icon. This opens the context menu. Select **veles** at the top of the menu (that’s our **veles.ovpn** profile) and choose **Connect**.  

A status window will open showing the log output while the connection is established, and a message will show once the client is connected.  

!!! tip "User Tip"
	Disconnect from the VPN the same way: Go into the system tray applet, right-click the OpenVPN applet icon, select the client profile and click **Disconnect**.

***

### Section D: Test VPN Connection

***Step 1***  

* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.

***

If you do, congratulations! You have now setup a Veles d-VPN . If you do not, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you.  
