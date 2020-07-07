Name:               Veles Android OpenVPN Guide
Image:              images/download/android.png
GuideType:          User's Guide
OS:                 Android
VelesdApp:          dVPN
Protocol:           OpenVPN
Requirements:       OpenVPN client
Difficulty:         Very Easy
EstimatedTime:      3 minutes


# Android OpenVPN Guide 
This will guide you through the process of installing and using OpenVPN on the Android platform.  

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) **Install OpenVPN Client**  
2) **Download Veles OpenVPN config**  

## Contents
* **Section A**: Download and Install OpenVPN
* **Section B**: Configure OpenVPN
* **Section C**: Connect to Veles dVPN
* **Section D**: Test VPN Connection
***

### Section A: Download and Install OpenVPN

***Step 1***

* Open the **Google Play Store**. Search for and install **Android OpenVPN Connect**, the official Android OpenVPN client application.

***

### Section B: Configure OpenVPN

***Step 1***  

* After installing OpenVPN, **download [Veles OpenVPN config file](https://explorer.veles.network/dapi/getOpenVPNConfig)**.  
[https://explorer.veles.network/dapi/getOpenVPNConfig](https://explorer.veles.network/dapi/getOpenVPNConfig)

***

***Step 2***  

* Start the **OpenVPN app** and tap the menu to **Import the profile**.

***

***Step 3***  

* **Then navigate to the location of the saved profile and select the file**. The app will make a note that the profile was imported.

***

### Section C: Connect to Veles dVPN 

***Step 1***  

* To connect, simply tap the **Connect** button. You’ll be asked if you trust the OpenVPN application. **Choose OK** to initiate the connection.  

!!! tip "User Tip"
	To **disconnect from the VPN**, go back to the OpenVPN app and choose **Disconnect**.  

***

### Section D: Test VPN Connection

***Step 1***  

* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.

***

If you do, congratulations! You have now setup a Veles dVPN . If you do not, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you.  
