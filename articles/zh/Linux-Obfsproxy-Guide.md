Name:               Veles Linux Obfsproxy Guide
Image:              https://www.veles.network/images/download/linux-wallet.png
GuideType:          User's Guide
OS:                 Linux
VelesdApp:          dVPN
Protocol:           Obfsproxy, OpenVPN
Requirements:       Obfsproxy, OpenVPN client
Difficulty:         Easy
EstimatedTime:      5 minutes

# Linux Obfsproxy Guide
This explains the process of installing Obfsproxy as a client in Linux.

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) **Succesfully installed [[Linux OpenVPN Guide]]**  
2) **Install Obfsproxy**  
3) **Download Veles shieled OpenVPN config**  

## Contents
* **Section A**: Download and Install Obfsproxy
* **Section B**: Configure Obfsproxy
* **Section C**: Connect Veles d-VPN with Obfsproxy
* **Section D**: Test VPN Connection
***

### Section A: Download and Install Obfsproxy

***Step 1***  

* On **Ubuntu or Debian**, you can install it just as you did on the server by typing:  
`sudo apt-get install obfsproxy`  

* On **CentOS** you can install Obfsproxy by typing:  
`yum install make automake gcc python-pip python-devel libyaml-devel`  
`pip install obfsproxy`    

* On **Arch Linux** you can install Obfsproxy from AUR package by typing:    
`yay --install obfsproxy-git`  

***

### Section B: Configure Obfsproxy

***Step 1***  

* **Download Veles Shielded configuration** file by typing:    
`wget https://explorer.veles.network/dapi/getShieldedOpenVPNConfig` 

***
  
***Step 2***  

* **Move downloaded config to it's repositories** by typing:    
`sudo mv shielded-veles.ovpn /etc/openvpn/client/`

***

### Section C: Connect Veles d-VPN with Obfsproxy

***Step 1***  

* Now, you can **connect to the VPN by just turning on ObfsProxy** and pointing the OpenVPN command to the client configuration file:  
`sudo obfsproxy scramblesuit --dest 80.211.132.243:21343 --password=SSSTIZ3LG5SSS43OMSSSM4LKGQFASSSS client 127.0.0.1:21337`    
`sudo openvpn --config /etc/openvpn/client/veles-shield.ovpn`  

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
