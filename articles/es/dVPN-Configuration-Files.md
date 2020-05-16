# Archivos de Configuración de dVPN

Para conocer como usar la dVPN de Veles y configurar tu cliente software, vea la [[Guía de Configuración de dVPN]] con las instrucciones para tu plataforma y el link de descarga específico.

Para un mejor entendimiento acerca de como los archivos de configuración y certificados de clientes son generados, continúa la lectura del artículo.

Tanto los certificados como los archivos de configuración son generados en el momento por masternodes Veles con soporte a dVPN seleccionados aleatoriamente.
Durante la actual etapa alpha de testeo, por razones de conveniencia se realizará el ruteo a través de uno de los gateways provistos por el equipo de desarrollo, pero usted puede igualmente seleccionar uno de su preferencia de la lista de masternodes activos con soporte a dVPN de la [lista extendida de masternodes](http://explorer.veles.network/dapi/mn/list/full) y utilizar la url provista.

Cuando la integración de la billetera GUI sea completada, alternativamente se podrá seleccionar un masternode desde la lista provista en la billetera y descargar de forma directa los archivos de configuración directamente desde la billetera.

## Elegir el masternode a utilizar (opcional)
Si quieres elegir un masternode específico de una locación específica, solamente debes abrir

y buscar un masternode con el servicio dVPN habilitado, por ejemplo:
```
        "80.211.5.147": {
   			...
            "services": {
            	...
                "services_available": [
                    "VPN"
                ]
            }
        }
```

## Descarga los archivos
Puedes clickear en *dAPI permalink* para descargar los archivos de configuración desde un masternode aleatorio.

Para descargar desde un masternode específicodebes ingresar la IO del masternode obtenida en el paso anterior en la url `https:// [ IP masternode ] / [ API URL abajo]` junto con la URL de la API debajo y abrir tu navegador.

Título                              | Link de dAPI                                                            | URL de API
----------------------------------- | ----------------------------------------------------------------------- |-------------------------------
Configuración OpenVPN               | [link](https://explorer.veles.network/dapi/getOpenVPNConfig)            | `api/getOpenVPNConfig` 
Configuración OpenVPN (stunnel)     | [link](https://explorer.veles.network/dapi/getOpenVPNShieldedConfig)    | `api/getOpenVPNShieldedConfig`
Configuracion Cliente Stunnel       | [link](https://explorer.veles.network/dapi/getStunnelConfig)            | `api/getStunnelConfig`
Certificado cliente Stunnel         | [link](https://explorer.veles.network/dapi/getStunnelCertificate)       | `api/getStunnelCertificate`

!!! tip "Nota de descarga manual"
    Cuando se descarga manualmente los archivos de configuración desde un masternode seleccionado, necesitarás aceptar la advertencia de que el host está utilizando un certificado no confiable - debido a que no requerimos a operadores de MN que adquieran nombres de dominio centralizados para sus nodos.
    
    Si ve el mensaje **Su conexión no es privada**, haga click en **Avanzado** y luego en **Proceder a X.Y.Z.W (no seguro)**. Su descarga debería ahora comenzar.
    
    Si lo quiere puede chequear que el certificado es emitido por **Veles Core dVPN CA**.
