Name:               Veles OSX OpenVPN Guide
Image:              https://www.veles.network/images/download/mac-wallet.png
TipoGuía:           Guía de Usuario
OS:                 Mac OSX
VelesdApp:          dVPN
Protocolo:          OpenVPN
Requerimientos:     Cliente OpenVPN
Dificultad:         Fácil
TiempoEstimado:     5 minutos

# Guía de OpenVPN para Linux
Esto te guiará a través del proceso de instalar y utilizar Tunnelblick en la plataforma OSX.  

Si requiere más ayuda por favor contacte a nuestro equipo de soporte @ [Discord](https://discord.gg/P528fGg)

## Requerimientos
1) **Instalar el cliente Tunnelblick**
2) **Descargar la configuración de Veles OpenVPN**

## Contenido
* **Sección A**: Descargar e instalar Tunnelblick
* **Sección B**: Configurar Tunnelblick
* **Sección C**: Conectarse a la dVPN de Veles
* **Sección D**: Testear la conexión VPN 
***

### Sección A: Descargar e instalar Tunnelblick

***Paso 1***  

* Tunnelblick es un cliente gratuito y open source de OpenVPN para Mac OS X. Puedes **descargar la última imagen de disco desde la [página de descargas de Tunnelblick](https://tunnelblick.net/downloads.html)**. Hacer doble click en el archivo **.dmg** descargado y seguir las instrucciones para instalar:  
[https://tunnelblick.net/downloads.html](https://tunnelblick.net/downloads.html)  

!!! tip "Tip de Usuario"
	Cerca del final del proceso de instalación, Tunnelblick preguntará si tienes algún archivo de configuración. Lo más sencillo es responder **No** y dejar que Tunnelblick finalice. 

***

### Sección B: Configurar Tunnelblick

***Paso 1***  

* Luego de instalar Tunnelblick, **descarga el [archivo de configuración de Veles OpenVPN](https://explorer.veles.network/dapi/getOpenVPNConfig)**.  
https://explorer.veles.network/dapi/getOpenVPNConfig

***Paso 2***  

* **Doble click en veles.ovpn**. Tunnelblick instalará el perfil de cliente.
  
!!! important "Importante"
	Se requieren privilegios administrativos. 

***

### Sección C: Conectarse a la dVPN de Veles

***Paso 1***  

* Ejecutar Tunnelblick mediante doble click en **Tunnelblick** en la **carpeta Aplicaciones**.

!!! tip "Tip de Usuario"
	Una vez que Tunnelblick se ejecutó, habrá un ícono de Tunnelblick en la barra de menú en la esquina superior derecha de la pantalla desde donde se podrá controlar las conexiones.

***

***Paso 2***  

* Click en el +icono, y luego en  **Conectar**  para iniciar la conexión VPN y seleccionar la conexión **veles**.  

***

### Sección D: Testear la conexión VPN 

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión VPN activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente VPN y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto, felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.   