Name:               Guía de Stunnel de Veles para OSX
Image:              https://www.veles.network/images/download/mac-wallet.png
TipoGuía:           Guía de Usuario
OS:                 Mac OSX
VelesdApp:          dVPN
Protocolo:          TLS/SSL (stunnel), OpenVPN
Requerimientos:     Stunnel, Cliente OpenVPN
Dificultad:         Fácil
TiempoEstimado:     5 minutos

# Guía de Stunnel para OSX
Esto te guiará a través del proceso de instalar y utilizar Stunnel en OSX.  

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

* Presionar **Command+Space**, tipear **Terminal** y presionar enter. En la Terminal ejecutar:  
`ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" < /dev/null 2> /dev/null`  

!!! important "Importante"
	Se requieren privilegios administrativos

***

***Paso 2***  

* Luego de que finalice la ejecución del anterior comando, **instalar Stunnel** mediante:  
`brew install stunnel`  

***

### Sección B: Configurar Veles Stunnel

***Paso 1***  

* **Descargar el [archivo de configuración de Stunnel para Veles](https://explorer.veles.network/dapi/getStunnelConfig)**:   
[https://explorer.veles.network/dapi/getStunnelConfig](https://explorer.veles.network/dapi/getStunnelConfig)  

***

***Paso 2***  

* **Mover las configuraciones descargadas a sus repositorios**: 
`/usr/local/etc/stunnel/`  
  
!!! tip "Tip de Usuario"
	necesitarás renombrar el archivo veles.stunnel.conf a stunnel.conf.

***

***Paso 3***  

* **Descargar la [configuración de Shielded OpenVPN para Veles](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)**:   
[https://explorer.veles.network/dapi/getShieldedOpenVPNConfig](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig) 

***

***Paso 4***  

* Tunnelblick **instalará el perfil de Veles Shielded OpenVPN** al hacer doble click en **veles-shielded.ovpn**.  

!!! important "Importante"
	Se requieren privilegios administrativos

***

### Sección C: Conectarse a la dVPN de Veles con Veles Stunnel

***Paso 1*** 

* Presionar **Command+Space**, tipear **Terminal** y presionar **enter**. Luego, iniciar Stunnel mediante:  
`stunnel`

***

***Paso 2***  

* Luego, ejecutar **Tunnelblick** mediante doble click en Tunnelblick en la carpeta de Aplicaciones.

***

***Psao 3***  

* Una vez que Tunnelblick se ejecutó, habrá un ícono de Tunnelblick en la barra de menú en la esquina superior derecha de la pantalla desde donde se podrá controlar las conexiones. Click en el ícono, y luego en el menú Conectar para iniciar la conexión VPN. Seleccionar la conexión **veles-shielded**.

***

### Sección D: Testear la conexión VPN 

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión VPN activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente VPN y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto, felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.   