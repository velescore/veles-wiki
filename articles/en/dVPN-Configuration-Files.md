# dVPN Configuration Files

To get information on how to use Veles dVPN and set-up your client software,
see [[dVPN Setup Guide]] with the instructions for your platform and specific
download link.

To understand more on how are configuration files and client certificates
generated, read on.


The certificates and configuration files generated on-the-fly by randomly
selected Veles Masternode with dVPN support. During current public alpha 
testing phase for convenience routed through one of our gateways provided by 
the development team, but you can also pick your own from one of the active 
masternodes with dVPN support from the 
[extended masternode list](http://explorer.veles.network/dapi/mn/list/full)
and use the url provided below.

When the integration into the GUI wallet will be completed, you'll also be 
able to pick the masternode from the list in GUI wallet and directly download
configuration files from the wallet.

## Pick your masternode (optional)
If you want to pick a specific masternode from specific location, just open
the 

and look for one with VPN Service enabled, for example:
```
        "80.211.5.147": {
   			...
            "services": {
            	...
                "services_available": [
                    "VPN"
                ]
            }
        }
```

## Download the files
You can click on *dAPI permalink* to download configuration files from a random
masternode.

To download from specific masternode you need to enter masternode IP from the step above 
into the url  `https:// [ masternode IP ] / [ API URL below]` alongside with the API URL 
below and open in your browser.

Title                               | dAPI link                                                               | API URL
----------------------------------- | ----------------------------------------------------------------------- | -------------------------------
OpenVPN config                      | [link](https://explorer.veles.network/dapi/getOpenVPNConfig)            | `api/getOpenVPNConfig` 
OpenVPN config (stunnel shielded)   | [link](https://explorer.veles.network/dapi/getOpenVPNShieldedConfig)    | `api/getOpenVPNShieldedConfig`
Stunnel client config               | [link](https://explorer.veles.network/dapi/getStunnelConfig)            | `api/getStunnelConfig`
Stunnel client certificate          | [link](https://explorer.veles.network/dapi/getStunnelCertificate)       | `api/getStunnelCertificate`

!!! tip "Manual Download Note"
    When manually downloading configuration files from chosen masternode, you will need to
    accept a warning that the host is using untrusted certificate - because we don't require
    MN operators to purchase centralized domain names for their nodes.

    If you see message **Your connection is not private**, click on **Advanced**
    button and on the **Proceed to X.Y.Z.W (unsafe)**. Now your download should begin.

    If you want you can double check that the certificate is issued by 
    the **Veles Core dVPN CA**.
