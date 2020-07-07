Name:               Guía de OpenVPN para Veles para Linux
Image:              images/download/linux-wallet.png
TipoGuía:           Guía de Usuario
OS:                 Linux
VelesdApp:          dVPN
Protocolo:          OpenVPN
Requerimientos:     Cliente OpenVPN
Dificultad:         Fácil
TiempoEstimado:     5 minutos

# Guía de OpenVPN para Linux

Si utilizas Linux, hay una gran variedad de herramientas que puedes utilizar dependiendo de tu distribución. Tu entorno de escritorio o tu administrador de redes puede también incluir utilidades de conexión. La forma más diseminada de conectarse, de todas formas, es utilizar el software OpenVPN.

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

#### Sección A: Descargar e instalar OpenVPN

***Paso 1*** 

* En **Ubuntu o Debian**, puedes instalar con el comando: 
```
sudo apt-get update
sudo apt-get install openvpn
```

* E **CentOS** puede habilitar los repositorios EPEL repositories y luego instalar mediante:
```
sudo yum install epel-release  
sudo yum install openvpn
```

* En **Gentoo** puedes instalar mediante:  
```
emerge -v net-vpn/openvpn
```

* En **Arch Linux** puedes instalar mediante:  
```
pacman -S openvpn
```

***

### Sección B: Configurar OpenVPN

***Paso 1***  

* **Generar un nuevo archivo de configuracion para Veles** (a través de nuestra dAPI desde un Masternode aleatorio) y **muevelo al repositorio** mediante:  
``wget https://explorer.veles.network/dapi/getOpenVPNConfig
sudo mv veles.ovpn /etc/openvpn/client/``

***

***Paso 2***  

* Setea el DNS para **mantenerse protegido de leaks de DNS** usando el siguiente comando ( **la IP usada en este caso sirve solamente de ejemplo y debe ser reemplazada por una de la lista de Masternodes** ):  
```echo -e "#Veles decentralized DNS\nnameserver 111.111.111.111" | sudo tee -a /etc/resolv.conf >> /dev/null```

***

### Sección C: Conectarse a la dVPN de Veles

***Paso 1***  

* Ahora, puedes **conectarte a la dVPN de Veles** apuntando el comando openvon al archivo de configuración de cliente:  
```openvpn --config /etc/openvpn/client/veles.ovpn```

***

### Sección D: Testear la conexión VPN 

***Paso 1***  

* Una vez que todo está instalado, es sencillo confirmar que todo está funcionando apropiadamente. Sin tener la conexión VPN activada, abra su navegador y vaya a [DNSLeakTest](https://www.dnsleaktest.com/).
El sitio le retornará la dirección IP asignada a usted por su proveedor de Internet, de la forma que el mundo lo ve. Para chequear su configuración de DNS a través del mismo sitio, clickee en Test Extendido y le informará que servidores DNS está utilizando.
Ahora, conecte su cliente VPN y refresque el navegador. La dirección IP totalmente nueva de su servidor VPN debería aparecer. Esto es como se muestra al mundo ahora. Nuevamente, el **Test Extendido** de  [DNSLeakTest](https://www.dnsleaktest.com/) chequeará su configuración de servidores DNS y le confirmará que está utilizando los resolvedores DNS de la dVPN Veles.

***

Si está todo correcto. felicitaciones! Has configurado la dVPN de Veles de manera exitosa. Si no es así, por favor contacta a soporte en [Discord](https://discord.gg/P528fGg) y ellos te asistirán.  
