Name:           Veles iOS OpenVPN Guide
Image:          https://www.veles.network/images/download/mac-wallet.png
Fecha:          Feb 12 2020,
Version: 		1.01
Sintaxis:       Markdown
Autores:        @AltcoinBaggins @mdfkbtc

# Guía de OpenVPN para iOS
Esto te guiará a través del proceso de instalar y utilizar OpenVPN en la plataforma iOS.  

Si requiere más ayuda por favor contacte a nuestro equipo de soporte @ [Discord](https://discord.gg/P528fGg)

## Requerimientos
1) **Instalar el cliente OpenVPN**  
2) **Descargar la configuración de OpenVPN de Veles**  

## Contenido
* **Sección A**: Descargar e instalar OpenVPN
* **Sección B**: Configurar OpenVPN
* **Sección C**: Conectarse a la dVPN de Veles
* **Sección D**: Testear la conexión VPN 
***

### Sección A: Descargar e instalar OpenVPN

***Paso 1***

* En la **App Store**, buscar e instalar **OpenVPN Connect**, el cliente oficial de OpenVPN para iOS.

***

### Sección B: Configurar OpenVPN

***Paso 1***  

* Luego de instalar OpenVPN Connect, **descarga el [archivo de configuración de OpenVPN para Veles](https://explorer.veles.network/dapi/getOpenVPNConfig)**.  
[https://explorer.veles.network/dapi/getOpenVPNConfig](https://explorer.veles.network/dapi/getOpenVPNConfig) y abrelo con **OpenVPN Connect** presionando **Copiar a OpenVPN**.  
[https://explorer.veles.network/dapi/getOpenVPNConfig](https://explorer.veles.network/dapi/getOpenVPNConfig)

***

***Paso 2***  

* Importar el archivo de perfil a OpenVPN Connect mediante la opción **Agregar**.

!!! tip "Tip de Usuario"
	Debería ver el mensaje **"Perfil importado exitosamente"**.

***

***Paso 3***  

* A continuación sólo debe **Agregar** el perfil a su OpenVPN Connect.

***

### Sección C: Conectarse a la dVPN de Veles

***Paso 1***  

* **Comience la conexión deslizando el botónde Conectar a la posición de Encendido**.  

!!! tip "Tip de Usuario"
	**Desconéctese** deslizando el mismo botón a **Apagado**.  

***

### Sección D: Testear la Conexión VPN

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión VPN activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente VPN y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto. felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.  

