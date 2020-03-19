Name:               Veles Linux Stunnel Guide
Image:              https://www.veles.network/images/download/linux-wallet.png
GuideType:          User's Guide
OS:                 Linux
VelesdApp:          dVPN
Protocol:           TLS/SSL (stunnel), OpenVPN
Requirements:       Stunnel, OpenVPN client
Difficulty:         Easy
EstimatedTime:      5 minutes

# Linux Stunnel Guide
This explains the process of installing Stunnel as a client in Linux.

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) **Succesfully installed [[OpenVPN]]**  
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

* On **Ubuntu or Debian**, you can install it just as you did on the server by typing:  
`sudo apt-get install stunnel`  

* On **CentOS** you can install Stunnel by typing:  
`yum install stunnel`  

* On **Arch Linux** you can install Stunnel by typing:  
`pacman -S stunnel` 

***

### Section B: Configure Stunnel

***Step 1***  

* **Download Veles Stunnel configuration files** by typing:  
`wget https://explorer.veles.network/dapi/getStunnelConfig`  
`wget https://explorer.veles.network/dapi/getShieldedOpenVPNConfig`  

***
  
***Step 2***  

* **Move downloaded configs to it's repositories** by typing:  
`sudo mv veles.stunnel.conf /etc/stunnel/stunnel.conf`    
`sudo mv shielded-veles.ovpn /etc/openvpn/client/`

***

### Section C: Connect Veles d-VPN with Stunnel

***Step 1***  

* Now, you can **connect to the VPN trough Stunnel** by just turning on Stunnel and pointing the OpenVPN command to the client configuration file:  
`sudo stunnel`  
`sudo openvpn --config /etc/openvpn/client/veles-shield.ovpn`

***

### Section D: Test VPN Connection

***Step 1***  

* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.

***

If you do, congratulations! You have now setup a . If you do not, please contact support on [Discord](https://discord.gg/P528fGg) and they will assist you.  
