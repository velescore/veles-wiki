Name:           Veles Android Stunnel Guide
Image:          https://www.veles.network/images/download/android.png
Date:           Feb 12 2020,
Version: 		1.01
Syntax:         Markdown
Authors:        @AltcoinBaggins @mdfkbtc

# Android Stunnel Guide 
This will guide you through the process of installing and using Stunnel on the Android platform.  

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) **Installed [[Android OpenVPN Guide]]**  
2) **Install Veles Stunnel**   
3) **Download Veles Shielded OpenVPN config**  

## Contents
* **Section A**: Download and Install Veles Stunnel
* **Section B**: Configure Veles Stunnel
* **Section C**: Connect to Veles d-VPN with Veles Stunnel
* **Section D**: Test VPN Connection
***

### Section A: Download and Install Veles Stunnel

***Step 1***  

* Open the **Google Play Store**. Search for and install **Veles Stunnel**, the official Veles Stunnel application.

***

### Section B: Configure Veles Stunnel

***Step 1***  

* After installing Veles Stunnel, **download [Shielded Veles OpenVPN config file](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)**.  
[https://explorer.veles.network/dapi/getShieldedOpenVPNConfig](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)

***

***Step 2***  

* Start the **OpenVPN app** and tap the menu to **Import the profile**.

***

***Step 3***  

* **Then navigate to the location of the saved profile and select the file**. The app will make a note that the profile was imported.

***

***Step 4***  

* **Start the Veles Stunnel app** and tap the menu to **Config**.

***

***Step 5***  

* Replace **"MasternodeIP"** with IP of masternode you are going to connect.  

!!! tip "User Tip"
	You can check the IP in OpenVPN Connect app when you import shielded-veles.ovpn profile  

***

### Section C: Connect to Veles d-VPN with Veles Stunnel 

***Step 1***  

* Now turn on Veles Stunnel . Open the app and **press the button on Home page**.

!!! tip "User Tip"
	**To disconnect** from the Veles Stunnel, just press that button on Home page again.  

***

***Step 2***  

* **To connect to VPN**, open OpenVPN Connect and simply tap the **Connect** button. You’ll be asked if you trust the OpenVPN application. Choose OK to initiate the connection.  

!!! tip "User Tip"
	**To disconnect from the VPN**, go back to the OpenVPN app and choose **Disconnect**.  

***

### Section D: Test VPN Connection

***Step 1***  

* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.

***

If you do, congratulations! You have now setup a Veles d-VPN . If you do not, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you.  
