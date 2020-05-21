Name:               Guía de Obfsproxy para Veles en Linux
Image:              https://www.veles.network/images/download/linux-wallet.png
TipodeGuía:          Guía de Usuario
OS:                  Linux
VelesdApp:           dVPN
Protocolo:           Obfsproxy, OpenVPN
Requirimientos:      clientes Obfsproxy, OpenVPN 
Dificultad:          Fácil
TiempoEstimado:      5 minutos

# Guía de Obfsproxy en Linux
Esta guía explica el proceso de instalar Obfsproxy como cliente en Linux.

Si requiere más ayuda por favor contacte a nuestro equipo de soporte @ [Discord](https://discord.gg/P528fGg) 

## Requirimientos
1) **Haber instalado satisfactoriamente lo indicado en la [[Guía de OpenVPN para Linux]]**  
2) **Instalar Obfsproxy**  
3) **Descargar la configuración de OpenVPN para Veles**  

## Contenido
* **Sección A**: Descargar e instalar Obfsproxy
* **Sección B**: Configurar Obfsproxy
* **Sección C**: Conectarse a la dVPN de Veles con Obfsproxy
* **Sección D**: Testear la conexión VPN 
***


### Sección A: Descargar e Instalar Obfsproxy

***Paso 1***  

* En **Ubuntu o Debian**, puedes instalar mediante el comando:  
`sudo apt-get install obfsproxy`  

* En **CentOS** puedes instalar Obfsproxy con el comando:  
`yum install make automake gcc python-pip python-devel libyaml-devel`  
`pip install obfsproxy`    

* En **Arch Linux** puedes instalar Obfsproxy desde el paquete AUR mediante el comando:    
`yay --install obfsproxy-git`  

***

### Sección B:  Configurar Obfsproxy

***Paso 1***  

* **Descargar la configuración para Veles** mediante:    
`wget https://explorer.veles.network/dapi/getShieldedOpenVPNConfig` 

***
  
***Paso 2***  

* **Mover el archivo de configuración descargado a los repositorios** mediante:    
`sudo mv shielded-veles.ovpn /etc/openvpn/client/`

***

### Sección C:  Conectar a la dVPN Veles con Obfsproxy

***Paso 1***  

* Ahora, puedes **conectarte a la VPN simplemente iniciando ObfsProxy** y apuntando el comando de OpenVPN la archivo de configuración de cliente:  
`sudo obfsproxy scramblesuit --dest 80.211.132.243:21343 --password=SSSTIZ3LG5SSS43OMSSSM4LKGQFASSSS client 127.0.0.1:21337`    
`sudo openvpn --config /etc/openvpn/client/veles-shield.ovpn`  

!!! tip "Tip de Usuario"
	La IP de destino (en este caso --dest 80.211.132.243) debe ser reempplazada con la **IP del masternode** al que se está conectando.  

!!! caution "Advertencia: Experimental"
	El password sólo será utilizando durante la etapa de testing pre-alpha. En el futuro en lugar de password se utilizará un string aleatorio.  

***
   
### Sección D: Testear la conexión Shadowsocks 

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión Shadowsocks activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente Shadowsocks y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto. felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.  
