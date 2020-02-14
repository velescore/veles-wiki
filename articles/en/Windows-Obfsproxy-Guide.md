Name:           Veles Windows Obfsproxy Guide
Image:          https://www.veles.network/images/download/windows-wallet.png
Date:           Feb 12 2020,
Version: 		1.01
Syntax:         Markdown
Authors:        @AltcoinBaggins @mdfkbtc

# Window Obfsproxy Guide
This explains the process of installing Obfsproxy as a client in Windows.

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) **Succesfully installed [[Windows OpenVPN Guide]]**  
2) **Install Obfsproxy**  
3) **Download Veles shieled OpenVPN config**  

## Contents
* **Section A**: Download and Install Obfsproxy
* **Section B**: Configure Obfsproxy
* **Section C**: Connect Veles d-VPN with Obfsproxy
* **Section D**: Test VPN Connection
***

### Section A: Download and Install Obfsporxy

***Step 1***  

* Now we are going build Obfsproxy. **Obfsproxy requires Python**, an open source programming language, so you’ll need to download it. Go to [python.org](https://www.python.org/downloads/) and **download version 2.7 and install** it accepting all the defaults:   
[https://www.python.org/downloads/](https://www.python.org/downloads/)

***

***Step 2***  

* You’ll also **need to get Visual C for Python**, which you can **download from [http://aka.ms/vcpython27](http://aka.ms/vcpython27)**, once you have downloaded it, install it with the default options:  

***

***Step 3***  

* Ok now that you have Python installed, you’re ready to get obfsproxy. Open a CMD shell window and **go to C:Python27Scripts** by typing :  
`cd C:\Python27\Scripts`

***

***Step 4***  

* Now we will **install Obfsproxy** by typing:  
`pip install obfsproxy`  

!!! tip "User Tip"
	This will download the various requisite modules and build obfsproxy – it might take a few minutes…… Once complete, you should have the **obfsproxy.exe** executable in **C:Python27Scripts**  

***

### Section B: Configure Obfsproxy

***Step 1***  

* After installing Obfsproxy **download [Shielded OpenVPN config](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)** from this URL:  
[https://explorer.veles.network/dapi/getShieldedOpenVPNConfig](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)  

***
  
***Step 2***  

* Move downloaded **veles-shielded.ovpn** config to it's repository:    
`C:\Program Files\OpenVPN\config\`    

***

### Section C: Connect Veles d-VPN with Obfsproxy

***Step 1***  

* Open a CMD shell window and **go to C:Python27Scripts** by typing:  
`cd C:\Python27\Scripts`    

***

***Step 2***  

* **Start Obfsproxy** by typing:  
`obfsproxy scramblesuit --dest 80.211.132.243:21343 --password=SSSTIZ3LG5SSS43OMSSSM4LKGQFASSSS client 127.0.0.1:21337`  

!!! tip "User Tip"
	The destination IP address (in this case --dest 80.211.132.243) should be replaced with **IP of masternode** you are connecting.    

!!! caution "Experimental Warning"
	The password will be used only in pre-alpha testing phase. In future instead of password will be used random string.  

***

### Section D: Test VPN Connection

***Step 1***  

* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.

***

If you do, congratulations! You have now setup a . If you do not, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you.  
