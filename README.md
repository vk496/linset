Linset Is Not a Social Enginering Tool
======

First of all, commented that this is a project for educational purposes that have served to me (and hopefully others) to be more in touch with the world of programming and Wireless. It is prohibited under any circumstances the use this tool in foregin Wireless Networks!



How it works
=======

- Scan the networks.
- Select network.
3. Capture handshake (can be used without handshake)
4. We choose one of several web interfaces tailored for me (thanks to the collaboration of the users)
5. Mounts one FakeAP imitating the original
6. A DHCP server is created on FakeAP
7. It creates a DNS server to redirect all requests to the Host
8. The web server with the selected interface is launched
9. The mechanism is launched to check the validity of the passwords that will be introduced
10. It deauthentificate all users of the network, hoping to connect to FakeAP and enter the password.
11. The attack will stop after the correct password checking


Are necessary tengais installed dependencies, which `Linset` check and indicate whether they are installed or not.

It is also preferable that you still keep the **patch for the negative channel**, because if not, you will have complications relizar to attack correctly


CHANGELOG
=======

```
########## 06-11-2013 LINSET 0.1
##
## #Fecha de Salida
##
########## 07-11-2013 LINSET 0.1b
##
## #Cambiado el Fakeweb a Inglés
## #Añadida funcion para quitar el modo monitor al salir
## #Arreglado Bucle para no colapsar la pantalla con información
## #Colocada opción de seleccionar otra red
## #Eliminado mensaje sobrante de iwconfig
##
########## 10-11-2013 LINSET 0.2
##
## #Añadido Changelog
## #Reestructurado el codigo
## #Cambiada la posición de ventanas xterm
## #Eliminada creacion extra del archivo route
## #Movido pantalla de comprobacion de handshake a una ventana xterm
## #Añadido menu durante el ataque
## #Añadida comprobacion de dependencias
##
########## 22-11-2013 LINSET 0.3
##
## #Arreglado mensaje de Handshake (no se mostraba bien)
## #Añadida interface de routers Telefonica y Jazztel (Xavi y Zyxel)
## #Fix cuando se usaba canales especificos (exit inesperado)
## #Mejorado DEBUG (function_clear y HOLD)
## #Migración de airbase-ng a hostapd
## #Reestructurado mas codigo
## #Añadido header
## #Añadida funcion para eliminar interfaces en modo monitor sobrantes
##
########## 30-11-2013 LINSET 0.4
##
## #Agregado soporte a airbase-ng junto a hostapd
## #Capacidad para comprobar pass sin handshake (modo Airlin"
## #Arregladas problemas con variables
## #Fix espacio Channel
## #Eliminada seleccion con multiples tarjetas de red
## #Arreglado error sintactico HTML de las interfaces Xavi
## #Implementada interface Zyxel (de routers de Telefonica también)
##
########## 07-12-2013 LINSET 0.5
##
## #Arreglado bug que impide usar mas de una interface
## #Migración de iwconfig a airmon-ng
## #Añadida interface HomeStation (Telefonica)
## #Arregladas llamadas PHP a error2.html inexistente
## #Arreglado bug que entraba en seleccion de Objetivos sin que se haya creado el CSV correspondiente
## #Opcion Salir en el menu de seleccion de webinterfaces
## #Arreglado bug que entraba en seleccion de Clientes sin que los haya
## #Arreglado bug que entraba en seleccion de Canal sin que haya interface valida seleccionada
##
########## 11-12-2013 LINSET 0.6
##
## #Bug al realizar deauth especifico sin que haya airodump en marcha
## #Modificadas variables que gestionan los CSV
## #Modificada estetica a la hora de seleccionar objetivo
## #Añadidos colores a los menus
## #Modificado funcionamiento interno de seleccion de opciones
## #Arreglado bug de variables en la comprobacion de dependencias
## #Añadida dependencia para ser root
##
########## 15-12-2013 LINSET 0.7
##
## #Añadido intro
## #Mejoradas variables de colores
## #Añadida interface de los routers Compal Broadband Networks (ONOXXXX)
## #Mejorada la gestion de la variable de Host_ENC
## #Arreglado bug que entraba en modo de FakeAP elegiendo una opcion inexistente
## #Modificado nombre de HomeStation a ADB Broadband (según su MAC)
## #Agregada licencia GPL v3
##
########## 27-12-2013 LINSET 0.8
##
## #Modificada comprobación de permisos para mostrar todo antes de salir
## #Añadida funcion para matar software que use el puerto 80
## #Agregado dhcpd a los requisitos
## #Cambiado titulo de dependecia de PHP (php5-cgi)
## #Modificado parametro deauth para PC's sin el kernel parcheado
## #Añadida funcion para matar software que use el puerto 53
## #Funcion para remontar los drivers por si se estaba usando la interface wireless
## #Modificada pantalla que comprueba el handshake (mas info) y mejoradas las variables
## #Mejorado menu de comprobacion de password con mas información
## #Añadida lista de clientes que se muestran en el menu de comprobacion de password
## #Cambiado ruta de guardado de password al $HOME
## #Reestructuracion completa del codigo para mejor compresion/busqueda
## #El intro no aparecerá si estas en modo desarrollador
## #No se cerrará el escaneo cuando se compruebe el handshake
#
## #Agregada funcion faltante a la 0.8 inicial (me lo comi sin querer)
##
########## 03-01-2014 LINSET 0.9
##
## #Funcion de limpieza si se cierra el script inesperadamente
## #Mejorada funcion de deteccion del driver
## #Modificadas variables que almacenaban las interfaces con nombres "wlan" y 'mon' para dar mas soporte a otros sistemass
## #La carpeta de trabajo se crea mas temprano para evitar posibles problemas
## #Añadida funcion para comprobar la ultima revision de LINSET
## #Autoactualizacion del script si detecta una version mas nueva de si mismo
## #Backup del script tras la actualizacion por si surgen problemas
## #Fix Menu de tipo de Desautentificacion (no se ve lo que se escribe)
## #Eliminada funcion handshakecheck del background
## #Eliminado mensaje de clientes.txt (problema devido a handcheck)
## #Bug que no mostraba correctamente los clientes conectados
##
########## 19-01-2014 LINSET 0.10
##
## #Agregado curl a las dependencias
## #Bug que no mostraba bien la lista de los clientes
## #Eliminado cuadrado en movimiento por cada sleep que se hacia en la ventana de comprobacion de handshake
## #Mejorada la comunicacion entre PHP y checkhandshake (ya no funciona por tiempos)
## #Cambiada ruta de trabajo de LINSET por defecto
## #Bug wpa_passphrase y wpa_supplicant no se cerraban tras concluir el ataque
## #Suprimidas de forma indefinida todas las interfaces web hasta ahora por motivos de copyright
## #Integrada interface web neutra basada en JQM
##
########## 29-01-2014 LINSET 0.11
##
## #Mejorada la comprobacion de actualizaciones (punto de partida desde la version del script actual)
## #Modificada url de comprobacion
## #Bug mensaje de root privilegies (seguia con el proceso)
## #Modificado orden de inicio (primero comprueba las dependencias)
## #Mejorada interface web
## #Agregada dependencia unzip
## #Bug al seleccionar una interface que no existe
## #Fix variable $privacy
## #Modificaciones leves de interface web
## #Adaptada interface para multiples idiomas
## #Añadido idioma Español
## #Añadido idioma Italiano
##
########## 18-02-2014 LINSET 0.12
##
## #Tarjetas con chipset 8187 pasaran dietctamente al menu de airbase-ng
## #Mensaje javascript adaptado según el idioma
## #Fix variable revision del backup
## #Bug en busqueda infinita de actualizaciones
## #Añadida restauracion de tput a la limpieza del script
## #Cerrar aplicaciones por medio del PID para evitar problemas
## #Añadido mdk3 a dependencias
## #Añadida desautenticacion por mdk3 al AP
## #Organizacion de codigo
## #Mejorada la busqueda de actualizaciones (casi directa)
## #Cambiada ruta de guardado del backup
##
########## 21-03-2014 LINSET 0.13
##
## #Ampliado tiempo de espera antes de detener el atque
## #Corregido bug al hacer backup
## #Añadido reinicio de NetworkManager para Wifislax 4.8
## #Desautentificacion masiva se hace exclusivamente con mdk3
## #Fallo al reiniciar networkmanager cuando acaba el ataque
## #Fix cuando se autocierra linset despues de acabar el ataque
## #Añadido pyrit a dependecias
## #Funcion de comprobacion estricta del handshake
## #Eliminadas dependencias inecesarias
## #Mayor desplazamiento por los menus
## #Añadido lenguaje Frances
## #Añadido lenguaje Portugues
##
##########
```

How to use
=======

```
$ chmod +x linset
$ ./linset
```
