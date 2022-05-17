## Práctica de laboratorio: configuración de los parámetros básicos del router con la CLI del IOS!

### Topología 

![](https://github.com/AbyssC1/pni26-alejandro/blob/main/Imagenes/UT7-A1/topologia.png)

### Tabla de direccionamiento

||||**Máscara de**|**Gateway**|
| :- | :- | :- | - | - |
|**Dispositivo**|**Interfaz**|**Dirección IP**|**subred**|**predeterminado**|
||||||
|R1|G0/0|192.168.0.1|255.255.255.0|N/A|
||G0/1|192.168.1.1|255.255.255.0|N/A|
|PC-A|NIC|192.168.1.3|255.255.255.0|192.168.1.1|
|PC-B|NIC|192.168.0.3|255.255.255.0|192.168.0.1|

### Objetivos

### Parte 1: establecer la topología e inicializar los dispositivos

- Realizar el cableado de los equipos para que coincidan con la topología de la red.  
- Inicializar y reiniciar el router y el switch.  

### Parte 2: configurar los dispositivos y verificar la conectividad

- Asignar información de IPv4 estática a las interfaces de la computadora.  
- Configurar los parámetros básicos del router.  
- Verificar la conectividad de la red  
- Configurar el router para el acceso por SSH.  

### Parte 3: mostrar la información del router

- Recuperar información del hardware y del software del router.  
- Interpretar el resultado de la configuración de inicio.  
- Interpretar el resultado de la tabla de routing.  
- Verificar el estado de las interfaces.  

### Parte 4: configurar IPv6 y verificar la conectividad

### Información básica/situación 

Esta es una práctica de laboratorio integral para revisar comandos de router de IOS que se abarcaron anteriormente. En las partes 1 y 2, realizará el cableado de los equipos y completará las configuraciones básicas y las configuraciones de las interfaces IPv4 en el router.

En la parte 3, utilizará SSH para conectarse de manera remota al router y usará comandos de IOS para recuperar la información del dispositivo para responder preguntas sobre el router. En la parte 4, configurará IPv6 en el router de modo que la PC-B pueda adquirir una dirección IP y luego verificará la conectividad.

Para fines de revisión, esta práctica de laboratorio proporciona los comandos necesarios para las configuraciones de router específicas.

**Nota**: los routers que se utilizan en las prácticas de laboratorio de CCNA son routers de servicios integrados** (ISR) Cisco 1941 con IOS de Cisco versión 15.2(4)M3 (imagen universalk9). Los switches que se utilizan son Cisco Catalyst 2960 con IOS de Cisco, versión 15.0(2) (imagen de lanbasek9). Se pueden utilizar otros routers, switches y otras versiones del IOS de Cisco. Según el modelo y la versión de IOS de Cisco, los comandos disponibles y los resultados que se obtienen pueden diferir de los que se muestran en las prácticas de laboratorio. Consulte la tabla Resumen de interfaces del router que se encuentra al final de esta práctica de laboratorio para obtener los identificadores de interfaz correctos.

**Nota**: asegúrese de que el router y el switch se hayan borrado y no tengan configuraciones de inicio.** Consulte el apéndice A para conocer los procedimientos para inicializar y volver a cargar los dispositivos.

### Recursos necesarios

- 1 router (Cisco 1941 con IOS de Cisco versión 15.2(4)M3, imagen universal o similar)  
- 1 switch (Cisco 2960 con IOS de Cisco versión 15.0(2), imagen lanbasek9 o comparable)  
- 2 computadoras (Windows 7, Vista o XP con un programa de emulación de terminal, como Tera Term)  
- Cables de consola para configurar los dispositivos con IOS de Cisco mediante los puertos de consola  
- Cables Ethernet, como se muestra en la topología  

**Nota**: las interfaces Gigabit Ethernet en los ISR Cisco 1941 cuentan con detección automática, y se puede** utilizar un cable directo de Ethernet entre el router y la PC-B. Si utiliza otro modelo de router Cisco, puede ser necesario usar un cable cruzado Ethernet.

### Parte 1:  establecer la topología e inicializar los dispositivos.

### Paso 1.  realizar el cableado de red tal como se muestra en la topología.

1. Conecte los dispositivos tal como se muestra en el diagrama de la topología y realice el cableado según sea necesario.  
2. Encienda todos los dispositivos de la topología.  

### Paso 2.  inicializar y volver a cargar el router y el switch.

**Nota**: en el apéndice A, se detallan los pasos para inicializar y volver a cargar los dispositivos.

### Parte 2:  Configurar dispositivos y verificar la conectividad.

### Paso 1.  Configure las interfaces de la PC.

1. Configure la dirección IP, la máscara de subred y la configuración del gateway predeterminado en la PC-A.  
1. Configure la dirección IP, la máscara de subred y la configuración del gateway predeterminado en la PC-B.  

### Paso 2.  Configurar el router.

:A:  Acceda al router mediante el puerto de consola y habilite el modo EXEC privilegiado.  

Router> **enable**  

Router#

:B:  Ingrese al modo de configuración global.  

Router# **config terminal**  

Router(config)#  

:C:  Asigne un nombre de dispositivo al router.  

Router(config)# **hostname R1**  

:D:  Deshabilite  la  búsqueda  DNS  para  evitar  que  el  router  intente  traducir  los  comandos incorrectamente introducidos como si fueran nombres de host.  

R1(config)# **no ip domain-lookup**  

:E:  Establezca el requisito de que todas las contraseñas tengan como mínimo 10 caracteres.  

R1(config)# **security passwords min-length 10**  

Además de configurar una longitud mínima, enumere otras formas de aportar seguridad a las contraseñas.

`Aparte  de  que  las  podemos  encriptar  es  necesario  que  estas  contraseñas  contenga  letras mayúsculas, números o caracteres para así dificultar la contraseña.`

:F:  Asigne **cisco12345** como la contraseña cifrada del modo EXEC privilegiado.  

R1(config)# **enable secret cisco12345**  

7. Asigne **ciscoconpass** como la contraseña de consola, establezca un tiempo de espera, habilite el inicio de sesión y agregue el comando **logging synchronous**. El comando **logging synchronous** sincroniza la depuración y el resultado del software IOS de Cisco, y evita que estos mensajes interrumpan la entrada del teclado.  

R1(config)# **line con 0**  

R1(config-line)# **password ciscoconpass**  

R1(config-line)#  **exec-timeout  5** 

**0** R1(config-line)# **login**  R1(config-line)# **logging synchronous**  

R1(config-line)# 

**exit** R1(config)#  

Para el comando **exec-timeout**, ¿qué representan el **5** y el **0**?  

``Que la sesión expirará en 5 minutos y 0 segundos``

8. Asigne **ciscovtypass** como la contraseña de vty, establezca un tiempo de espera, habilite el inicio de sesión y agregue el comando **logging synchronous**.  

R1(config)# **line vty 0 4**  

R1(config-line)# **password ciscovtypass** 

R1(config-line)#  **exec-timeout  5** **0** 

R1(config-line)# **login**  

R1(config-line)# **logging synchronous**  

R1(config-line)# **exit** R1(config)#  

9. Cifre las contraseñas de texto no cifrado.  

R1(config)# **service password-encryption**  

![](https://github.com/AbyssC1/pni26-alejandro/blob/main/Imagenes/UT7-A1/1configuracion%20de%20reouter.png)

10. Cree un aviso que advierta a todo aquel que acceda al dispositivo que el acceso no autorizado está prohibido.  

### Práctica de laboratorio: configuración de los parámetros básicos del router con la CLI del IOS!.

R1(config)# **banner motd #Unauthorized access prohibited!#**

11. Configure una dirección IP y una descripción de interfaz. Active las dos interfaces en el router.  

R1(config)# **int g0/0**  

R1(config-if)# **description Connection to PC-B** 

R1(config-if)# **ip address 192.168.0.1 255.255.255.0** 

R1(config-if)# **no shutdown** 

R1(config-if)# **int g0/1** 

R1(config-if)# **description Connection to S1** 

R1(config-if)# **ip address 192.168.1.1 255.255.255.0** 

R1(config-if)# **no shutdown** 

R1(config-if)# **exit** 

R1(config)# **exit**  

R1#  

12. Configure el reloj en el router, por ejemplo:  R1# **clock set 17:00:00 18 Feb 2013**  
13. Guarde la configuración en ejecución en el archivo de configuración de inicio.  R1# **copy running-config startup-config**  

Destination  filename  [startup- config]? Building configuration... [OK] 

R1#  

¿Qué resultado obtendría al volver a cargar el router antes de completar el comando **copy running- config startup-config**?**  

**Se borraría toda la configuración que se realice, ya que el router no tendría una configuración de inicio.**

**Paso 3.  Verificar la conectividad de la red**

1. Haga ping a la PC-B en un símbolo del sistema en la PC-A. 

**Nota:** quizá sea necesario deshabilitar el firewall de las computadoras.

** ¿Tuvieron éxito los pings? 

**Si**

Después de completar esta serie de comandos, ¿qué tipo de acceso remoto podría usarse para acceder al R1?

**Telnet**

2. Acceda de forma remota al R1 desde la PC-A mediante el cliente de Telnet de Tera Term.  

Abra Tera Term e introduzca la dirección IP de la interfaz G0/1 del R1 en el campo Host: de la ventana Tera Term: New Connection (Tera Term: nueva conexión). Asegúrese de que el botón de opción **Telnet** esté seleccionado y después haga clic en **OK** (Aceptar) para conectarse al router.  

¿Pudo conectarse remotamente? 

**Si**

¿Por qué el protocolo Telnet es considerado un riesgo de seguridad?

**Porque las contraseñas no están cifradas, es decir pueden verse fácilmente mediante un programa.**

**Paso 4.  configurar el router para el acceso por SSH.**

1. Habilite las conexiones SSH y cree un usuario en la base de datos local del router.  

R1# **configure terminal**  

R1(config)# **ip domain-name CCNA-lab.com**  

R1(config)# **username admin privilege 15 secret adminpass1**  

R1(config)# **line vty 0 4**  

R1(config-line)# **transport input ssh**  

R1(config-line)#  **login local** 

R1(config-line)# **exit**  

R1(config)# **crypto key generate rsa modulus 1024**  

R1(config)# **exit**  

2. Acceda remotamente al R1 desde la PC-A con el cliente SSH de Tera Term.  

Abra Tera Term e introduzca la dirección IP de la interfaz G0/1 del R1 en el campo Host: de la ventana Tera Term: New Connection (Tera Term: nueva conexión). Asegúrese de que el botón de opción **SSH** esté seleccionado y después haga clic en **OK** para conectarse al router.  

¿Pudo conectarse remotamente? \_\_\_\_

**Parte 3:  mostrar la información del router**

En la parte 3, utilizará comandos **show** en una sesión SSH para recuperar información del router.

**Paso 1.  establecer una sesión SSH para el R1.**

Mediante Tera Term en la PC-B, abra una sesión SSH para el R1 en la dirección IP 192.168.0.1 e inicie sesión como **admin** y use la contraseña **adminpass1**.

**Paso 2.  recuperar información importante del hardware y el software.**

1. Use el comando **show version** para responder preguntas sobre el router. 

¿Cuál es el nombre de la imagen de IOS que el router está ejecutando?  

``c1900-uiversalk9-mz.SPA.151-1.M4.bin``

¿Cuánta memoria de acceso aleatorio no volátil (NVRAM) tiene el router? 

``255Kbytes``

¿Cuánta memoria flash tiene el router?  

``249856Kbytes``

2. Con frecuencia, los comandos **show** proporcionan varias pantallas de resultados. Filtrar el resultado permite que un usuario visualice determinadas secciones del resultado. Para habilitar el comando de filtrado, introduzca una barra vertical (**|**) después de un comando **show**, seguido de un parámetro de filtrado y una expresión de filtrado. Para que el resultado coincida con la instrucción de filtrado, puede usar la palabra clave **include** para ver todas las líneas del resultado que contienen la expresión de filtrado. Filtre el comando **show version** mediante **show version | include register** para responder la siguiente pregunta.  

¿Cuál es el proceso de arranque para el router en la siguiente recarga?  

``No se puede realizar simulando con el Packet Tracer, no ejecuta el comando.``

**Paso 3.  mostrar la configuración de inicio.**

Use el comando **show startup-config** en el router para responder las siguientes preguntas. 

¿De qué forma figuran las contraseñas en el resultado?

``Se encuentran encriptadas.``

Use el comando **show startup-config | begin vty**. 

¿Qué resultado se obtiene al usar este comando?

``No se puede realizar simulando con el Packet Tracer, no ejecuta el comando.``

**Paso 4.  mostrar la tabla de routing en el router.**

Use el comando **show ip route** en el router para responder las siguientes preguntas. 

¿Qué código se utiliza en la tabla de routing para indicar una red conectada directamente? 

``Con la letra C se indica que hay una subred conectada directamente``

¿Cuántas entradas de ruta están cifradas con un código C en la tabla de routing? 

``2``

**Paso 5.  mostrar una lista de resumen de las interfaces del router.**

Use el comando **show ip interface brief** en el router para responder la siguiente pregunta.

¿Qué comando cambió el estado de los puertos Gigabit Ethernet de administrativamente inactivo a activo?

``no shutdown``

**Parte 4:  configurar IPv6 y verificar la conectividad**

**Paso 1.  asignar direcciones IPv6 a la G0/0 del R1 y habilitar el routing IPv6.**

**Nota:** la asignación de una dirección IPv6, además de una dirección IPv4, en una interfaz se conoce como** “dual stacking”, debido a que las pilas de protocolos IPv4 e IPv6 están activas. Al habilitar el routing de unidifusión IPv6 en el R1, la PC-B recibe el prefijo de red IPv6 de G0/0 del R1 y puede configurar automáticamente la dirección IPv6 y el gateway predeterminado.

1. Asigne una dirección de unidifusión global IPv6 a la interfaz G0/0; asigne la dirección link-local en la interfaz, además de la dirección de unidifusión; y habilite el routing IPv6.  

R1# **configure terminal** 

R1(config)# **interface g0/0** 

R1(config-if)#  **ipv6  address  2001:db8acad:a::1/64** 

R1(config-if)# **ipv6 address fe80::1 link-local** 

R1(config-if)# **no shutdown** 

R1(config-if)# **exit** 

R1(config)# **ipv6 unicast-routing**  

R1(config)# **exit**  

2. Use el comando **show ipv6 int brief** para verificar la configuración de IPv6 en el R1. Si no se asignó una dirección IPv6 a la G0/1, ¿por qué se indica como [up/up]?  

**Es el estado de la capa 1 y la capa 2 de la interfaz y no depende de la capa 3.**

3. Emita el comando **ipconfig** en la PC-B para examinar la configuración de IPv6. 

¿Cuál es la dirección IPv6 asignada a la PC-B?  

**FE80::204:9AFF:FE5C:4C79**

¿Cuál es el gateway predeterminado asignado a la PC-B? 

``192.168.0.1``

En la PC-B, haga ping a la dirección link-local del gateway predeterminado del R1. 

¿Tuvo éxito? 

``Si*`` 

En la PC-B,

 haga ping a la dirección IPv6 de unidifusión del R1 2001:db8:acad:a::1.

¿Tuvo éxito? 

``No``

### Reflexión

1. Durante la investigación de un problema de conectividad de red, un técnico sospecha que no se habilitó una interfaz. 

¿Qué comando **show** podría usar el técnico para resolver este problema?  

``show ip interface brief o show startup-config``

2. Durante la investigación de un problema de conectividad de red, un técnico sospecha que se asignó una máscara de subred incorrecta a una interfaz. 

¿Qué comando **show** podría usar el técnico para resolver este problema?  

``show startup-config o show running-config``

3. Después de configurar IPv6 en la LAN de la PC-B en la interfaz G0/0 del R1, si hiciera ping de la PC-A a la dirección IPv6 de la PC-B, ¿el ping sería correcto? ¿Por qué o por qué no?  

``Fallaría ya que la interfaz g0/1 no se configure con ipv6 y la PC-A solo tiene una dirección ipv4.``

**Tabla de resumen de interfaces del router** 

|**Resumen de interfaces del router**|
| - |
|**Modelo de router**|**Interfaz Ethernet #1**|**Interfaz Ethernet n.º 2**|**Interfaz serial #1**|**Interfaz serial n.º 2**|
|1800|Fast Ethernet 0/0 (F0/0)|Fast Ethernet 0/1 (F0/1)|Serial 0/0/0 (S0/0/0)|Serial 0/0/1 (S0/0/1)|
|1900|Gigabit Ethernet 0/0 (G0/0)|Gigabit Ethernet 0/1 (G0/1)|Serial 0/0/0 (S0/0/0)|Serial 0/0/1 (S0/0/1)|
|2801|Fast Ethernet 0/0 (F0/0)|Fast Ethernet 0/1 (F0/1)|Serial 0/1/0 (S0/1/0)|Serial 0/1/1 (S0/1/1)|
|2811|Fast Ethernet 0/0 (F0/0)|Fast Ethernet 0/1 (F0/1)|Serial 0/0/0 (S0/0/0)|Serial 0/0/1 (S0/0/1)|
|2900|Gigabit Ethernet 0/0 (G0/0)|Gigabit Ethernet 0/1 (G0/1)|Serial 0/0/0 (S0/0/0)|Serial 0/0/1 (S0/0/1)|
|**Nota**: para conocer la configuración del router, observe las interfaces a fin de identificar el tipo de router y** cuántas interfaces tiene. No existe una forma eficaz de confeccionar una lista de todas las combinaciones de configuraciones para cada clase de router. En esta tabla, se incluyen los identificadores para las posibles combinaciones de interfaces Ethernet y seriales en el dispositivo. En esta tabla, no se incluye ningún otro tipo de interfaz, si bien puede haber interfaces de otro tipo en un router determinado. La interfaz BRI ISDN es un ejemplo. La cadena entre paréntesis es la abreviatura legal que se puede utilizar en los comandos de IOS de Cisco para representar la interfaz.|
**Apéndice A: inicialización y recarga de un router y un switch** **Paso 1.  inicializar y volver a cargar el router.**

1. Acceda al router mediante el puerto de consola y habilite el modo EXEC privilegiado.  Router> **enable** 

Router# 

2. Escriba el comando **erase startup-config** para eliminar el archivo de configuración de inicio de la NVRAM.  

Router# **erase startup-config**  

Erasing  the  nvram  filesystem  will  remove  all  configuration  files!  Continue? [confirm] [OK] 

Erase of nvram: complete 

Router# 

3. Emita el comando **reload** para eliminar una configuración antigua de la memoria. Cuando reciba el mensaje **Proceed with reload** (Continuar con la recarga), presione Enter para confirmar. (Si presiona cualquier otra tecla, se cancela la recarga).  

Router# **reload**  

Proceed with reload? [confirm]  

\*Nov  29  18:28:09.923:  %SYS-5-RELOAD:  Reload  requested  by  console.  Reload Reason: Reload Command. 

**Nota:** es posible que reciba un mensaje para guardar la configuración en ejecución antes de volver a** cargar el router. Escriba **no** y presione Enter.

System configuration has been modified. Save? [yes/no]: **no**

4. Una vez que se vuelve a cargar el router, se le solicita introducir el diálogo de configuración inicial. Escriba **no** y presione Enter.  

Would you like to enter the initial configuration dialog? [yes/no]: **no**

5. Se le solicita finalizar la instalación automática. Escriba **yes** (sí) y, luego, presione Enter.  Would you like to terminate autoinstall? [yes]: **yes**

**Paso 2.  inicializar y volver a cargar el switch.**

1. Acceda al switch mediante el puerto de consola e ingrese al modo EXEC privilegiado.  Switch> **enable** 

Switch# 

2. Utilice el comando **show flash** para determinar si se crearon VLAN en el switch.  Switch# **show flash**  

Directory of flash:/ 

2 -rwx 1919 Mar 1 1993 00:06:33 +00:00 private-config.text

3 -rwx 1632 Mar 1 1993 00:06:33 +00:00 config.text

4 -rwx 13336 Mar 1 1993 00:06:33 +00:00 multiple-fs

5 -rwx 11607161 Mar 1 199302:37:06 +00:00  c2960-lanbasek9-mz.150-2.SE.bin 6 -rwx 616 Mar 1 199300:07:13 +00:00 vlan.dat

32514048 bytes total (20886528 bytes free) 

Switch#

3. Si se encontró el archivo **vlan.dat** en la memoria flash, elimínelo.  Switch# **delete vlan.dat**  

Delete filename [vlan.dat]? 

4. Se le solicitará que verifique el nombre de archivo. En este momento, puede cambiar el nombre de archivo o, simplemente, presionar Enter si introdujo el nombre de manera correcta.  
5. Se le solicitará que confirme que desea eliminar este archivo. Presione Enter para confirmar la eliminación. (Si se presiona cualquier otra tecla, se anula la eliminación).  

Delete  flash:/vlan.dat? 

[confirm] Switch# 

6. Utilice el comando **erase startup-config** para eliminar el archivo de configuración de inicio de la NVRAM. Se le solicitará que confirme la eliminación del archivo de configuración. Presione Enter para confirmar que desea borrar este archivo. (Al pulsar cualquier otra tecla, se cancela la operación).  

Switch# **erase startup-config**  

Erasing  the  nvram  filesystem  will  remove  all  configuration  files!  Continue? [confirm] [OK] 

Erase of nvram: complete 

Switch# 

7. Vuelva a cargar el switch para eliminar toda información de configuración antigua de la memoria. Se le solicitará que confirme la recarga del switch. Presione Enter para seguir con la recarga. (Si presiona cualquier otra tecla, se cancela la recarga).  

Switch# **reload**

Proceed with reload? [confirm]

**Nota:** es posible que reciba un mensaje para guardar la configuración en ejecución antes de volver a** cargar el switch. Escriba **no** y presione Enter.

System configuration has been modified. Save? [yes/no]: **no**

8. Una vez que se vuelve a cargar el switch, se le solicita introducir el diálogo de configuración inicial. Escriba **no** y presione Enter.  

Would you like to enter the initial configuration dialog? [yes/no]: **no**

Switch>  
