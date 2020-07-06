Name:               Guía Linux de Obfsproxy para Veles
Image:              https://www.veles.network/images/download/linux-wallet.png
TipoGuía:    		Guía de Usuario
OS:                 Linux
VelesdApp:          dVPN
Protocolos:         Obfsproxy, OpenVPN
Requerimientos:     Obfsproxy, cliente OpenVPN
Dificultad:         Fácil
TiempoEstimado:     5 minutos

# Guía de Obfsproxy para Linux

Esta guía explica el proceso de instalación de Obfsproxy como cliente en Linux.

Si requiere más ayuda por favor contacte a nuestro equipo de soporte @ [Discord](https://discord.gg/P528fGg)

## Requirimientos

1) **Tener instalado [[Guía de OpenVPN para Linux]]**  
2) **Instalar Obfsproxy**   
3) **Descargar la configuración de Shielded OpenVPN para Veles**  

## Contenido

* **Sección A**: Descargar e instalar Obfsproxy
* **Sección B**: Configurar Obfsproxy
* **Sección C**: Conectarse a la dVPN de Veles con Obfsproxy
* **Sección D**: Testear la conexión VPN 

***

### Sección A: Descargar e instalar Obfsproxy

***Paso 1*** 

* En **Ubuntu o Debian**, puedes instalar de la misma forma que lo hiciste en el servidor con el comando:  
`sudo apt-get install obfsproxy`  

* En **CentOS** puedes instalar Obfsproxy con los comandos:  
`yum install make automake gcc python-pip python-devel libyaml-devel`  
`pip install obfsproxy`    

* En **Arch Linux** puedes instalar Obfsproxy desde el paquete AUR mediante:    
`yay --install obfsproxy-git`  

***

### Sección B: Configurar Obfsproxy

***Paso 1***  

* **Descarga el [archivo de configuración de Stunnel para Veles](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)** mediante:    
`wget https://explorer.veles.network/dapi/getShieldedOpenVPNConfig` 

***
  
***Paso 2***  

* **Mover el archivo de configuración descargado a sus repositorios** mediante:    
`sudo mv shielded-veles.ovpn /etc/openvpn/client/`

***

### Sección C: Conectarse a la dVPN de Veles con Veles Stunnel

***Paso 1***  

* Ahora puede **conectarse a la dVPN simplemente iniciando ObfsProxy** y direccionando el comando de OpenVPN al archivo de configuración de cliente:  
`sudo obfsproxy scramblesuit --dest 80.211.132.243:21343 --password=SSSTIZ3LG5SSS43OMSSSM4LKGQFASSSS client 127.0.0.1:21337`    
`sudo openvpn --config /etc/openvpn/client/veles-shield.ovpn`  

!!! tip "Tip de Usuario"
	La IP de destino (en este caso --dest 80.211.132.243) debe ser reemplazada por la **IP del masternode** al que se está conectando.  

!!! caution "Experimental"
	La contraseña será usada en la fase de testeo pre-alpha. En el futuro en lugar de un passsword se utilizará un string aleatorio.

***


### Sección D: Testear la conexión VPN 

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión VPN activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente VPN y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto. felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.   
