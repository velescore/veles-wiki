Name:               Guía Linux de Veles en Stunnel
Image:              https://www.veles.network/images/download/linux-wallet.png
TipoGuía:           Guía de Usuario
OS:                 Linux
VelesdApp:          dVPN
Protocolo:          TLS/SSL (stunnel), OpenVPN
Requerimientos:     Stunnel, Cliente OpenVPN
Dificultad:         Fácil
TiempoEstimado:     5 minutos

# Guía de Stunnel para Linux
Esto te guiará a través del proceso de instalar y utilizar Stunnel en Linux.  

Si requiere más ayuda por favor contacte a nuestro equipo de soporte @ [Discord](https://discord.gg/P528fGg)

## Requerimientos
1) **Instalación exitosa de [[OpenVPN]]**  
2) **Instalar Stunnel**  
3) **Descargar la configuración de Shielded OpenVPN para Veles** 
4) **Descargar la configuración de Stunnel para Veles**   

## Contenido
* **Sección A**: Descargar e instalar Veles Stunnel
* **Sección B**: Configurar Veles Stunnel
* **Sección C**: Conectarse a la dVPN de Veles con Veles Stunnel
* **Sección D**: Testear la conexión VPN 
***

### Sección A: Descargar e instalar Veles Stunnel

***Paso 1*** 

* En **Ubuntu o Debian**, puedes instalarlo de la misma manera que en el servidor mediante:  
`sudo apt-get install stunnel`  

* En **CentOS** puedes instalar Stunnel mediante:  
`yum install stunnel`  

* On **Arch Linux** puedes instalar Stunnel mediante:  
`pacman -S stunnel` 

***

### Sección B: Configurar Veles Stunnel

***Paso 1***  

* **Descarga los archivos de configuración de Stunnel para Veles** mediante:  
`wget https://explorer.veles.network/dapi/getStunnelConfig`  
`wget https://explorer.veles.network/dapi/getShieldedOpenVPNConfig`  

***
  
***Paso 2***  

* **Mover las configuraciones descargadas a sus repositorios** mediante:  
`sudo mv veles.stunnel.conf /etc/stunnel/stunnel.conf`    
`sudo mv shielded-veles.ovpn /etc/openvpn/client/`

***

### Sección C: Conectarse a la dVPN de Veles con Veles Stunnel

***Paso 1*** 

* Ahora, puedes **conectar a la VPN a través de Stunnel** iniciando Stunnel y apuntando el comando de OpenVPN al archivo de configuracion de cliente:  
`sudo stunnel`  
`sudo openvpn --config /etc/openvpn/client/veles-shield.ovpn`

***

### Sección D: Testear la conexión VPN 

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión VPN activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente VPN y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto. felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.   
