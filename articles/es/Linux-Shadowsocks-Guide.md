Name:               Guía de Shadowsocks en Linux para Veles
Image:              https://www.veles.network/images/download/linux-wallet.png
TipoGuía:           Guía de Usuario
OS:                 Linux
VelesdApp:          dVPN
Protocolo:          Shadowsocks
Requirimientos:     cliente Shadowsocks
Dificultad:         Fácil
TiempoEstimado:     5 minutos

# Guía de Shadowsocks para Linux
Esto te guiará a través del proceso de instalar y utilizar Shadowsock en la plataforma Linux.  

Si requiere más ayuda por favor contacte a nuestro equipo de soporte @ [Discord](https://discord.gg/P528fGg) 

## Requirimientos
1) **Instalar el cliente de Shadowsocks**  
2) **Descargar la configuración de OpenVPN para Veles** 

## Contenido
* **Sección A**: Descargar e instalar Shadowsocks
* **Sección B**: Configurar Shadowsocks
* **Sección C**: Conectarse a la dVPN de Veles con Shadowsocks
* **Sección D**: Testear la conexión Shadowsocks 
***

### Sección A: Descargar e instalar Shadowsocks

***Paso 1***

* En **Ubuntu o Debian**, puedes instalarlo mediante el comando:  
`sudo apt install shadowsocks`  

* En **CentOS** puedes habilitar los repositorios EPEL y luego instalarlo mediante:  
`sudo yum install epel-release`  
`sudo yum install m2crypto python-setuptools`  
`sudo yum install python-pip`  
`pip install shadowsocks`  

* En **Arch Linux**, puedes instalarlo mediante el comando:  
`pacman -S shadowsocks-libev`  

***

### Sección B: Configurar Shadowsocks

***Paso 1***   

* Luego de instalar el cliente de Shadowsocks, **descarga el [archivo de configuración de Shadowsocks para Veles](https://explorer.veles.network/dapi/getShadowsocksConfig)**.  
[https://explorer.veles.network/dapi/getShadowsocksConfig](https://explorer.veles.network/dapi/getShadowsocksConfig)

***

***Paso 2***    

* **Abrir la configuración de Shadowsocks** con tu editor favorito. La misma se encuentra en:  
`nano /etc/shadowsocks.json`

***

***Paso 3***  

* Luego, completa el **"Hostname" (nombre de host)** con la **IP del Masternode** en la configuración de Shadowsocks.

***

***Paso 4***  

* Reemplazar **"Remote Port" (Puerto Remoto)** con el Puerto Remoto de Veles **21344**

***

***Paso 5***  

* Cambiar **"Encryption Method" (Método de Encriptación)** a **aes-256-cfb**

***

***Paso 6***  

* Completar el **"Password"** con el password en la configuración de Shadowsocks.  

!!! caution "Advertencia: Experimental"
	En fase de testeo la contraseña por defecto es - **`password`**  

***

### Sección C: Conectarse a la dVPN de Veles con Shadowsocks

***Paso 1***

* **Para conectarte**, dimplemente ejecuta el comando **sslocal** para iniciar el cliente ShadowSocks:    
`sslocal -c /etc/shadowsocks/config.json`  

!!! tip "Tip de Usuario"
	En caso de ver los siguientes mensajes significa que el cliente inicio correctamente.  
	`INFO: loading config from /etc/shadowsocks/config.json`  
	`2018-10-01 21:28:25 INFO loading libcrypto from libcrypto.so.1.1`  
	`2018-10-01 21:28:25 INFO starting local at 127.0.0.1:1080`    

***

### Sección D: Testear la conexión Shadowsocks 

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión Shadowsocks activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente Shadowsocks y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto. felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.  

