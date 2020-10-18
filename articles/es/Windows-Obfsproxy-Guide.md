Name:               Veles Windows Obfsproxy Guide
Image:              https://www.veles.network/images/download/windows-wallet.png
TipoGuía:    		User's Guide
OS:                 Windows
VelesdApp:          dVPN
Protocolos:         Obfsproxy, OpenVPN
Requerimientos:     Obfsproxy, cliente OpenVPN
Dificultad:         Fácil
TiempoEstimado:     5 minutos

# Guía de Obfsproxy para Windows

Esta guía explica el proceso de instalación de Obfsproxy como cliente en Windows.

Si requiere más ayuda por favor contacte a nuestro equipo de soporte @ [Discord](https://discord.gg/P528fGg)

## Requirimientos

1) **Tener instalado [[Guía de OpenVPN para Windows]]**  
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

* Comenzaremos con Obfsproxy. **Obfsproxy requiere Python**, un lenguaje de programación de código abierto, por lo que deberás descargarlo. Vé a [python.org](https://www.python.org/downloads/) y **descarga e instala la versión 2.7** utilizando la configuración por defecto:   
[https://www.python.org/downloads/](https://www.python.org/downloads/)

***

***Paso 2***  

* También **necesitarás Visual C para Python**, el cuál puedes **descargar desde [http://aka.ms/vcpython27](http://aka.ms/vcpython27)**. Una vez que lo hayas descargado, instálalo con la configuración por defecto:  

***

***Paso 3***  

* Ya con Python instalado, estás en condiciones de instalar Obfsproxy. Abrir una consola de comandos y **vé a C:Python27Scripts** mediante :  
`cd C:\Python27\Scripts`

***

***Paso 4***  

* Ahora **instalaremos Obfsproxy** mediante:  
`pip install obfsproxy`  

!!! tip "Tip de Usuario"
	Ésto descargará varios módulos requeridos y creará el ejecutable de obfsproxy – puede demorar unos minutos…… Una vez completo, deberías tener el ejecutable **obfsproxy.exe** en **C:Python27Scripts**  

***

### Sección B: Configurar Obfsproxy

***Paso 1***  

* **Descarga el [archivo de configuración de Stunnel para Veles](https://explorer.veles.network/dapi/getShieldedOpenVPNConfig)** mediante:    
`wget https://explorer.veles.network/dapi/getShieldedOpenVPNConfig` 

***
  
***Paso 2***  

* **Mover el archivo de configuración descargado veles-shielded.ovpn a sus repositorios** en:    
`C:\Program Files\OpenVPN\config\`

***

### Sección C: Conectarse a la dVPN de Veles con Veles Stunnel

***Paso 1***   

* Abrir una consola de comandos e **ir a C:Python27Scripts** mediante:  
`cd C:\Python27\Scripts`    

***

***Paso 2***  

* **Start Obfsproxy** mediante:  
`obfsproxy scramblesuit --dest 80.211.132.243:21343 --password=SSSTIZ3LG5SSS43OMSSSM4LKGQFASSSS client 127.0.0.1:21337`  

!!! tip "Tip de Usuario"
	La IP de destino (en este caso --dest 80.211.132.243) deberá ser reemplazada con la **IP del masternode** al que te estás conectando.    

!!! caution "Advertencia: Experimental"
	La contraseña será utilizada en la fase de testeo pre-alpha. En el futuro en lugar de password se utilizará un string aleatorio. 

***

### Sección D: Testear la conexión VPN 

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión VPN activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente VPN y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto. felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.   

