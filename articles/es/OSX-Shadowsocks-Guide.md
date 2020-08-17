Name:               Guía de Shadowsocks de Veles para OSX
Image:              https://www.veles.network/images/download/mac-wallet.png
TipoGuía:           Guía de Usuario
OS:                 Mac OSX
VelesdApp:          dVPN
Protocolo:          Shadowsocks
Requirimientos:     Cliente Shadowsocks
Dificultad:         Fácil
TiempoEstimado:     5 minutos

# Guía de Shadowsocks para OSX
Esto te guiará a través del proceso de instalar y utilizar Shadowsock en la plataforma OSX.  

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

* **Descarga e instala [ShadowsocksX-NG](https://github.com/shadowsocks/ShadowsocksX-NG/releases)**:
[https://github.com/shadowsocks/ShadowsocksX-NG/releases](https://github.com/shadowsocks/ShadowsocksX-NG/releases)

***

### Sección B: Configurar Shadowsocks

***Paso 1***   

* Luego de instalar ShadowsocksX-NG, **desacrge el [archivo de configuración de Shadowsocks para Veles](https://explorer.veles.network/dapi/getShadowsocksConfig)**.  
[https://explorer.veles.network/dapi/getShadowsocksConfig](https://explorer.veles.network/dapi/getShadowsocksConfig)

***

***Paso 2***  

* Click en **Servidores —> Preferencia de Servidores**

***

***Paso 3***  

* Presionar **+** para agregar un nuevo perfil

***

***Paso 4***  

* Luego, completa el **"Hostname"** con la **IP del Masternode** que se encuentra en la configuración de Shadowsocks Config.

***

***Paso 5***  

* Reemplazar **"Remote Port" (Puerto Remoto)** con el Puerto Remoto de Veles **21344**

***

***Step 6***  

* Cambiar **"Encryption Method" (Método de Encriptación)** a **aes-256-cfb**

***

***Step 7***  

* Completar el **"Password"** con el password en la configuración de Shadowsocks.  

!!! caution "Advertencia: Experimental"
	En fase de testeo la contraseña por defecto es - **`password`** 

***

### Sección C: Conectarse a la dVPN de Veles con Shadowsocks

***Paso 1***

* Para conectarte, simplemente presiona el botón **Conectar**. 

***

### Sección D: Testear la conexión Shadowsocks 

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión Shadowsocks activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente Shadowsocks y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto, felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.  