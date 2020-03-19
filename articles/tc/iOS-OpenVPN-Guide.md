Name:           Veles iOS OpenVPN Guide
Image:          https://www.veles.network/images/download/mac-wallet.png
Date:           Feb 12 2020,
Version: 		1.01
Syntax:         Markdown
Authors:        @AltcoinBaggins @mdfkbtc

# iOS OpenVPN Guide 
This will guide you through the process of installing and using OpenVPN on the iOS platform.  

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

* From the **App Store**, search for and install **OpenVPN Connect**, the official iOS OpenVPN client application.

***

### Section B: Configure OpenVPN

***Step 1***  

* After installing OpenVPN Connect, **download [Veles OpenVPN config file](https://explorer.veles.network/dapi/getOpenVPNConfig)** and open with **OpenVPN Connect** by pressing **Copy to OpenVPN**.  
[https://explorer.veles.network/dapi/getOpenVPNConfig](https://explorer.veles.network/dapi/getOpenVPNConfig)

***

***Step 2***  

* Import profile file into OpenVPN Connect by pressing **Add**.

!!! tip "User Tip"
	You should see **"Profile successfully imported"**.

***

***Step 3***  

* Now just **Add** profile to your OpenVPN Connect.

***

### Section C: Connect to Veles d-VPN 

***Step 1***  

* **Start the connection by sliding the Connect button to the On position**.  

!!! tip "User Tip"
	**Disconnect** by sliding the same button to **Off**.  

***

### Section D: Test VPN Connection

***Step 1***  

* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.

***

If you do, congratulations! You have now setup a Veles d-VPN . If you do not, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you.  
