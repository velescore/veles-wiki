Name:               Veles Core Masternode Guide
Image:              https://veles.network/images/mn/veles-mnguide-thumb.png
TipoGuía:           Guía de Operador de Maseternode
OS:                 Linux
Generación:			1ra
Requerimientos:     500 VLS, VPS/server, Billetera local, cliente SSH
Dificultad:         Fácil
TiempoEstimado:      5 minutos

# Guía de masternodes para Linux

Este es un tutorial paso a paso acerca de cómo configurar un Masternode de Veles en un servidor Linux, utilizando el script de [Instalación de Masternode de Veles](https://github.com/Velescore/veles-masternode-install) script.

Si requiere más ayuda por favor contacte a nuestro equipo de soporte @ [Discord](https://discord.gg/P528fGg)


## Distribuciones Linux soportadas
* **Ubuntu**
* **Debian**
* **Linux Mint**
* **Gentoo**
* **Sabayon**
* **Fedora**
* **RHEL**
* **CentOS**

## Requerimientos
1) **500 VLS**  
2) **VPS corriendo Linux (de los mencionados anteriormente)**  
3) **Una billetera local**  
4) **Un cliente SSH tal como [PuTTY](https://the.earth.li/~sgtatham/putty/0.72/w64/putty-64bit-0.72-installer.msi) o [BitVise](https://dl.bitvise.com/BvSshClient-Inst.exe)**  
***

## Contenido
* **Sección A**: Descargando e instalando BitVise
* **Sección B**: Conectándose al VPS a instalando el script via BitVise
* **Sección C**: Preparando la billetera local
* **Sección D**: Conectándose e iniciando el masternode
***

### Sección A: Descargando e instalando BitVise

***Paso 1***  

* Descarga BitVise [here](https://dl.bitvise.com/BvSshClient-Inst.exe)  

***

### Sección B: Conectándose al VPS a instalando el script via BitVise


***Paso 1***  

* Abrir la aplicación bitvise y completar el **"Hostname"** con la **IP de tu VPS**

![Example-PuttyInstaller](/images/guides/mn1.png)  

***

***Paso 2***  

* Copiar la **password de root** de tu VPS

![Example-RootPass](/images/guides/mn2.png)

***

***Paso 3***

* Ingresar **"root"** en el login/nombre de usuario

![Example-Root](/images/guides/mn3.png)  

***

***Paso 4***  

* Pegar el password en la terminal Bitvise terminal mediante click derecho (no mostrará el password así que sólo presionar enter)

![Example-RootPassEnter](/images/guides/mn4.png)

***

***Paso 5***  

* Una vez que presiones abrir mostrará una alerta de seguridad (**clickear Sí**)   

***

***Paso 6***  

* **Pegar el siguiente código** en la terminal de Bitvise y luego presionar enter y esperar:  
`source <(curl -s https://raw.githubusercontent.com/velescore/veles-installer/master/masternode.sh)`

![Example-RootPassEnter](/images/guides/mn5.png)  

***

***Paso 7***  

* Ingresar tu **Private Key de Masternode** de Veles o dejar en blanco para generar una nueva password aleatoriamente

![Example-RootPassEnter](/images/guides/mn6.png)

***

### Sección C: Preparando la billetera local

***Paso 1***  

* Descarga e instala la billetera Veles [aquí](https://veles.network/download.html)

***

***Paso 2***  

* Generar una nueva dirección a través de la consola mediente el comando:   
`getnewaddress "MN1" "legacy"`  

* Enviar exactamente **500 VLS** a la dirección generada en tu billetera local

![Example-console](/images/guides/mn7.png)  

***

***Paso 3***  

* Ir a la consola dentro de la billetera e ingresas el siguiente comando:  
`masternode outputs`  

![Example-outputs](/images/guides/mn8.png)  

***

***Paso 4***  

* Copiar la **ID de transacción y el output index**

***

### Sección D: Conectándose e iniciando el masternode 

***Paso 1***  

* Ir a la pestaña **"herramientas"** dentro de la billetera y abrir el **"archivo de configuracion de masternode"**  

***

***Paso 2***  

* Completar el formulario. 
* Para `Alias` ingresar algo cómo "MN01" **sin usar espacios**
* La `Dirección` es la **IP de tu server** (se encontrará en la terminal de Bitvise que deberás todavia tener abierta).
* La `PrivKey` es tu **clave privada de masternode** (también en la terminal de Bitvise).
* La `TxHash` es la **Id de transacción/clave** que copiaste. en el archivo de configuración
* El `Output Index` es el **0 o 1** que copiaste en el archivo de configuración.

![Example-create](/images/guides/mn9.png)

* Clickear **"Guardar Archivo"**  

***

***Paso 3***  

* Cerrar y abrir nuevamente la billetera
* Clickes en la pestaña de Masternodes **"Mis masternodes"**
* Chequear si la transacción del colateral de tu Masternode tiene **16 confirmaciones**
* Clickear start alias  en la **pestaña masternodes**

![Example-create](/images/guides/mn10.png)

***

***Paso 4***  

* Conectar tu VPS y **cambiar tu user de root a veles** mediante:    
`su veles` 

* Chequear el **status de tu masternode** dentro del VPS mediante el comando:  
`veles-cli masternode status`  
  
* Comandos de usuario de Veles:   
`veles-cli masternode status` #Chequear estado del masternode 
`veles-cli getblockchaininfo` #Información general cómo la versión de Veles y el número de bloque actual
`veles-cli mnsync status` #Chequear si el MN esta sincronizado con la cadena.  

* Comandos como usuario Root:  
`systemctl status veles.service` #Chequear si el servicio Veles esta corriendo
`systemctl start veles.service` #Iniciar el servicio Veles
`systemctl stop veles.service` #Detener el servicio Veles
`systemctl is-enabled veles.service` #Chequear si el servicio se ejecuta al iniciar el SO

***

Si está todo correcto. felicitaciones! Has configurado el MN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán. 
