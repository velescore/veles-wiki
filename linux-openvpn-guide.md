
# Linux OpenVPN Guide 

If you are using Linux, there are a variety of tools that you can use depending on your distribution. Your desktop environment or network manager might also include connection utilities. The most universal way of connecting, however, is to just use the OpenVPN software.

If you require further assistance contact the support team @ [Discord](https://discord.gg/P528fGg)

## Requirements
1) Install OpenVPN Client
2) Download Veles OpenVPN config
***

## Contents
* **Section A**: Download and Install OpenVPN
* **Section B**: Configure OpenVPN
* **Section C**: Connect to Veles d-VPN
* **Section D**: Test VPN Connection
***

### Section A: Download and Install OpenVPN

***Step 1***
* On Ubuntu or Debian, you can install it by typing:  
`sudo apt-get update`  
`sudo apt-get install openvpn`  
* On CentOS you can enable the EPEL repositories and then install it by typing:  
`sudo yum install epel-release`  
`sudo yum install openvpn`  
* On Gentoo you can install it by typing:  
`emerge -v net-vpn/openvpn`  
* On Arch Linux you can install it by typing:  
`pacman -S openvpn`  
***

### Section B: Configure OpenVPN 

***Step 1***
* Download Veles configuration file and move to it's repository by typing:  
`wget https://explorer.veles.network/dapi/getOpenVPNConfig`  
`sudo mv veles.ovpn /etc/openvpn/client/`
***

***Step 2***
* Setup DNS to stay protected against DNS leaks use this command ( **IP used in this case serve only as example and need to replaced by one from new Masternode list** ):  
`echo -e "#Veles decentralized DNS\nnameserver 111.111.111.111" | sudo tee -a /etc/resolv.conf >> /dev/null`
***

### Section C: Connect to Veles d-VPN
***Step 1***
* Now you can connect to the Veles d-VPN by just pointing the openvpn command to the client configuration file:  
`openvpn --config /etc/openvpn/client/veles.ovpn`
***

### Section D: Test VPN Connection

***Step 1***
* Once everything is installed, a simple check confirms everything is working properly. Without having a VPN connection enabled, open a browser and go to [DNSLeakTest](https://www.dnsleaktest.com/).
The site will return the IP address assigned by your internet service provider and as you appear to the rest of the world. To check your DNS settings through the same website, click on Extended Test and it will tell you which DNS servers you are using.
Now connect to your VPN client and refresh the browser. The completely different IP address of your VPN server should now appear. That is now how you appear to the world. Again, [DNSLeakTest's](https://www.dnsleaktest.com/) **Extended Test** will check your DNS settings and confirm you are now using the DNS resolvers pushed by Veles dVPN.
***

If you do, congratulations! You have now setup a Veles d-VPN . If you do not, please contact support and they will assist you.  
***