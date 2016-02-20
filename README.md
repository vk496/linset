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

Script for install dependencies (Dependences.sh)
=======
Check the installation and if not automatically download and install the necessary software for use linset.

```
$ chmod +x Dependences.sh
$ ./Dependences.sh
```

=======

```
########## 06-11-2013 LINSET 0.1
##
## #Fecha de Salida
##
########## 31-10-2014 LINSET 0.15 **last version**
##
## #Mas info a la hora de elegir una interfaz wireless
## #Capacidad de intentar confirmar handshake local con aircrack-ng
## #Añadido SIGHUP
## #Arreglado problema de desautentificaciones mdk3
## #Mejorado contador de tiempo
##
##########
```

How to use
=======

```
$ chmod +x linset
$ ./linset
```
