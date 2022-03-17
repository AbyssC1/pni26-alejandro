<center>

# Packet Tracer


</center>

***Nombre:***
***Curso:*** 1º de Ciclo Superior de Administración de Sistemas Informáticos en Red.

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

En esta practica usaremos varios dispositivos para crear una red y saber su funcionamiento.

#### ***Objetivos***. <a name="id2"></a>

Los objetivos de esta practica es aprender el funcionamiento de una red y sus equipos

#### ***Material empleado***. <a name="id3"></a>

El material empleado fue el "Packet Tracer" 

#### ***Desarrollo***. <a name="id4"></a>

<h1>Ejercicio 1. Comandos importantes. Ping, tracert y
pathping.</h1>

Paso 1. Realizar un ping, desde la máquina virtual, a las siguientes direcciones, 
comprobando los mensajes que devuelven cada uno de ellos. Se recomienda analizar 
porque se produce cada respuesta:
<p>• 192.168.1.250
<p>• 172.20.1.2
<p>• www.google.es (responde)
<p>• www.gobiernodecanarias.org (tiempo de espera agotado, pero traduce)
<p>• www.educacion.es (tiempo de espera agotado, pero traduce)
<p>• www.iespuertodelacruz.com (dirección no existente)
<p>• leela.servidor
<p>Paso 2. Realizar un tracert a las direcciones dadas anteriormente y explicar los 
resultados.
<p>Paso 3. Realizar un pathping a las direcciones dadas anteriormente.

![alt text](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20Tracer%20img%201/Practica%201.png "IMG")
  
  
<h1>Ejercicio 2. Tipos de cables en uniones entre equipos.</h1>
  
<p>Vamos a verificar los cables que se necesitan colocar, utilizando par trenzado, en la 
comunicación entre diferentes dispositivos.
  
<p>Paso 1. Unión de un PC con otro. Utilizar el cable adecuando de par trenzado hasta 
que se produzca comunicación (luces en verde en ambos extremos).
<p>Paso 2. Unión de un PC con un switch (utilizaremos un 2950‐24 para todas las 
experiencias). Utilizar el cable adecuando de par trenzado hasta que se produzca 
comunicación (luces en verde en ambos extremos).
<p>Paso 3. Unión de un switch con otro. Utilizar el cable adecuando de par trenzado 
hasta que se produzca comunicación (luces en verde en ambos extremos).
<p>Paso 4. Unión de un PC con un router (utilizaremos el 1841 en todas las 
experiencias). Utilizar el cable adecuando de par trenzado hasta que se produzca 
comunicación (luces en verde en ambos extremos).
<p>Paso 5. Unión de un switch con un router. Utilizar el cable adecuando de par 
trenzado hasta que se produzca comunicación (luces en verde en ambos extremos).
<p>Paso 6. Unión de un switch con un hub (utilizaremos el HUB‐PT). Utilizar el cable 
adecuando de par trenzado hasta que se produzca comunicación (luces en verde en 
ambos extremos)

![Ejercicio 2](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20tracer%20PKT%201/Ejercicio%202.pkt "IMG")
  
  
<h1>Ejercicio 3. Diferencias entre Hub y Switch.</h1>

<p>En esta primera práctica intentaremos ver la diferencia entre Switch y Hub. Para ello 
realizaremos las siguientes acciones:
  
<p>Paso1. Añadimos un Generic Hub‐PT, que nos presenta un pequeño hub con 6
puertos Fast Ethernet.
<p>Paso 2. Añadimos 3 ordenadores con las siguientes configuraciones:
Nombre Dirección IP Máscara de red
  
PC01 192.168.5.101 255.255.255.0
PC02 192.168.5.102 255.255.255.0
PC03 192.168.5.103 255.255.255.0
<p>Paso 3. Conectar los 3 equipos con el hub utilizando el cableado adecuado.
<p>Paso 4. Comprobar la conectividad entre los equipos realizando un ping entre ellos.
<p>Paso 5. Una vez comprobada la conectividad, pasar del modo Tiempo Real al modo 
Simulación y volver a realizar un ping entre equipos. Se debe reiniciar la configuración 
para poder apreciar los paquetes ICMP entre los equipos. Para realizar correctamente 
esta experiencia, y no tener más información que la necesaria, aplicar un filtro de 
eventos que sólo nos presente los paquetes ARP e ICMP (que son los necesarios para 
comprobar el funcionamiento del ping). Comprobar también tablas ARP aprendidas,
ejecutando el comando arp -a en uno de los equipos.
<p>Paso 6. Realizar las mismas pruebas cambiando el Generic Hub‐PT por un switch 2950‐
24. Grabar el proyecto con un nuevo nombre. Comprobar la diferencia entre ambas 
experiencias
  
![Ejercicio 3](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20tracer%20PKT%201/Ejercicio%203.pkt "IMG") 
  
  
![Ejercicio 3.2](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20tracer%20PKT%201/Ejercicio%203%2C2.pkt "IMG") 
  
<h1>Ejercicio 4. Unión entre switchs de comunicaciones.</h1>

<p>El ejercicio nos sirve para comprobar las diferentes uniones entre varios switchs de 
comunicaciones.
<p>Paso 1. Colocar 4 switchs 2950‐24, cambiando sus nombres a SW01, SW02, SW03 y 
SW04.
<p>Paso 2. Realizar las siguientes conexiones entre switchs:
Switch origen Puerto destino Puerto origen Switch destino Puerto destino Puerto destino
<p>SW01 2 SW02 1
<p>SW01 3 SW03 1
<p>SW02 4 SW04 2
<p>Paso 3. Insertar los siguientes equipos con sus correspondientes configuraciones:
Nombre IP Máscara Switch Puerto
<p>PC01 10.0.1.101 255.255.0.0 SW01 11
<p>PC02 10.0.2.102 255.255.0.0 SW02 12
<p>PC03 10.0.3.103 255.255.0.0 SW03 13
<p>PC04 10.0.4.104 255.255.0.0 SW04 14
<p>Paso 4. Comprobar la conectividad de los 4 equipos.
<p>Paso 5. Introducir una nueva conexión entre switchs entre el SW01 puerto 4 y el 
SW04 puerto 1. Esto crea un circuito entre los equipos. Comprobar qué sucede con la 
comunicación entre equipos.
<p>Paso 6. Eliminar la última conexión realizada. Añadir un Generic Hub‐PT y 
denominarlo HUB05. Utilizando el puerto 1 de este hub, unirlo al SW04 puerto 1. 
Insertar un nuevo equipo con la configuración PC05, 10.0.5.105, 255.255.0.0, al puerto 
del hub número 5. Comprobar la conectividad de los 4 equipos anteriores con éste
  
 ![Ejercicio 4](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20Tracer%20img%201/Ejercicio%204.png "IMG")
 
 ![Ejercicio 4](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20tracer%20PKT%201/Ejercicio%204.pkt "IMG")
  
<h1>Ejercicio 5. Direccionamiento IP.</h1>

<p>Partiendo de una configuración de 3 switchs y 15 equipos, comprobar la comunicación 
entre los equipos mediante el uso de direcciones IP y máscaras.
 
<p>Paso 1. Insertar tres switchs 2950‐24 con los nombres SW01, SW02 y SW03, con la 
siguiente configuración:
<p>Switch origen Puerto origen Switch destino Puerto destino
SW01 2 SW02 1
SW01 3 SW03 1
<p>Paso 2. Insertar los 15 equipos con la siguiente configuración:
Nombre IP Máscara Switch Puerto
<p>PC01 192.168.1.101 255.255.255.0 SW01 11
<p>PC02 192.168.1.121 255.255.255.248 SW02 11
<p>PC03 192.168.1.140 255.255.255.192 SW03 11
<p>PC04 192.168.1.160 255.255.255.128 SW01 12
<p>PC05 192.168.1.1 255.255.255.0 SW02 12
<p>PC06 192.168.1.11 255.255.255.224 SW03 12
<p>PC07 192.168.1.111 255.255.255.128 SW01 13
<p>PC08 192.168.1.200 255.255.255.240 SW02 13
<p>PC09 192.168.1.201 255.255.255.0 SW03 13
<p>PC10 192.168.1.248 255.255.255.128 SW01 14
<p>PC11 192.168.1.144 255.255.255.192 SW02 14
<p>PC12 192.168.1.211 255.255.255.240 SW03 14
<p>PC13 192.168.1.25 255.255.255.128 SW01 15
<p>PC14 192.168.1.33 255.255.255.224 SW02 15
<p>PC15 192.168.1.222 255.255.255.0 SW03 15
<p>Paso 3. Calcular, de forma manual, qué equipos se comunican entre ellos. 
Comprobar estos cálculos con los aportados por las comunicaciones del ejemplo.
<p>Paso 4. Comprobar las direcciones MAC que 
ha aprendido cada uno de los switchs. Para ello, 
entramos en el modo consola de cada uno de 
los switchs.
  
<p>Dentro de ese modo consola, debemos entrar 
en el modo privilegiado del sistema. Esto se 
consigue tecleando el comando enable. 
Después, al cambiar el prompt de petición a 
tener un #, colocaremos el comando show 
mac‐address‐table.
Verificamos que los resultados eran los 
requeridos.
<p>Señalar que, si no hay comunicación entre los equipos durante un tiempo, esta tabla se 
vacía.
<p>Comprobar también que en los equipos podemos verificar las relaciones direcciones IP 
y MAC de los equipos con los que nos hemos comunicado mediante el comando 
arp –a.
<p>Sobre la máquina virtual (no sobre el simulador) realizamos un ping a la dirección 
www.google.es. Este ping debe ser correcto. Comprobar y explicar qué elementos 
aparecen al realizar el comando arp –a después de esta comunicación.
<p>Paso 5. Cambiar la configuración de tal forma que los equipos se comuniquen en 
grupos de 5 equipos (primer grupo PC01 al PC05, segundo grupo PC06 al PC10, tercer 
grupo PC11 al PC15)

 ![Ejercicio 5](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20Tracer%20img%201/practica%205%20switch%201.png "IMG")  
  
 ![Ejercicio 5](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20Tracer%20img%201/Practica%205%20switch%202.png "IMG")
  
 ![Ejercicio 5](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20Tracer%20img%201/practica%205%20switch%203.png "IMG")
  
 ![Ejercicio 5](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20tracer%20PKT%201/Ejercicio%205.pkt "IMG") 
  
  <h1>Ejercicio 6. Seguridad y configuraciones de un switch.</h1>
  
<p>Como es lógico, el acceso a un switch lo realizaremos desde un equipo exterior, ya que 
el propio switch no presenta ninguna pantalla. Para ver esto en el simulador, 
colocaremos un PC y un switch, y los uniremos mediante un cable de consola (por el 
puerto RS232 o puerto COM1 del equipo y por el puerto de consola del switch).
  
<p>Esta unión la usaremos entrando en el PC y utilizando la opción de Terminal. En un PC 
real, lo haríamos utilizando el aplicativo Hiperterminal.
Dejaremos la configuración de velocidad, bits de datos, paridad, etc. que se nos ofrece 
por defecto.
  
<p>Paso 1. Establecer la conexión con el switch utilizando la opción de enlace por Consola 
y Terminal.
<p>Paso 2. Establecer el nombre del equipo. Este es uno de los primeros pasos que se 
suele realizar al configurar un switch. En nuestro caso, le pondremos el nombre 
Mi_primer_switch. Esta acción la realizamos desde el modo comando de la siguiente 
forma:
<p>Switch> enable (entra en el modo privilegiado de configuración)
<p>Switch# configure terminal (entra en el modo de configuración que es el que permite 
el cambio de los parámetros del switch)
<p>Switch(config)# hostname Mi_primer_switch (cambia el nombre) 
<p>Mi_primer_switch (config)# (vemos como ya ha cambiado el nombre)
<p>Paso 3. Desactivar avisos de consola. Es una acción muy habitual, ya que, con cada 
modificación del estado de alguno de los parámetros del switch, se presenta un 
mensaje por consola. Por ejemplo, cuando apagamos o encendemos un equipo, se 
presentan mensajes del estado de ese puerto en el que estaba conectado el equipo. 
Debemos comprobar que esto es así, y, usando los comandos siguientes, 
comprobaremos que ya no se presentan dichas alertas.
<p>Switch> enable
<p>Switch# configure terminal
<p>Switch(config)# no logging console (para la aparición de mensajes por consola)
4
<p>Paso 4. Contraseñas de acceso. Si nuestro switch es una parte importante de nuestra 
configuración de red, es lógico que protejamos su acceso mediante el uso de 
contraseñas.
<p>En primer lugar, podemos establecer una contraseña para acceder al modo 
privilegiado. Esto lo hacemos con los siguientes comandos:
<p>Switch> enable
<p>Switch# configure terminal
<p>Switch(config)# enable secret ciscoenable (activa y fija la contraseña del modo 
privilegiado a ciscoenable)
Y después activamos la contraseña para la entrada mediante consola:
<p>Switch(config)# line console 0 (se puede colocar una contraseña diferente para 
cada tipo de acceso; nosotros estamos entrando por consola; ver que cambia el 
prompt del sistema)
<p>Switch(config)# password cisco (coloca como contraseña la palabra cisco) 
<p>Switch(config‐line)# login (activa la solicitud de contraseña por consola)
<p>Debemos comprobar que esto funciona, por lo que nos desconectaremos de la consola 
y volveremos a entrar.
<p>Para desactivar la contraseña del modo consola, llegando a config‐line tecleamos no 
login. Para desactivar la contraseña del modo privilegiado, llegando a config tecleamos 
no enable secret.
<p>La mayoría de los desactivados en IOS CISCO se hacen colocando el comando no por 
delante del comando que lo activó.
<p>Paso 5. Configurar dirección IP, máscara y puerta de enlace del switch.
La dirección IP del propio switch la configuramos para su acceso a través de la VLAN1. 
Por eso, muchos fabricantes, llaman a esta VLAN1 la de gestión, ya que el 
equipamiento de red configura por ahí su acceso remoto por IP.
<p>En modo comando, lo hacemos así:
<p>Switch> enable
<p>Switch# configure terminal
<p>Switch(config)# interface vlan 1 (entramos en la configuración de la vlan 1) 
<p>Switch(config‐if)#ip address 192.168.1.254 255.255.255.0 (colocamos la IP y la 
máscara)
<p>Switch(config‐if)# no shutdown (este comando activa el interface que acabamos 
de configurar)
<p>Switch(config)# exit (salimos a la configuración general)
<p>Switch(config)# ip default‐gateway 192.168.1.1 (configuramos la puerta de enlace 
predeterminada para todas las comunicaciones de gestión del switch; hay que 
colocarlo si queremos acceder a él a través de un router, o para que se conecte a 
Internet para descargar actualizaciones, etc.)
<p>Podemos comprobar que la IP funciona realizando un ping desde un equipo que esté 
enganchado al switch.

<p>Paso 6. Guardar la configuración.
Con todos los pasos anteriores, hemos modificado la configuración de nuestro switch, 
pero existe un problema: no hemos guardado la configuración.
Para verificar que esto es así, procedemos a recargar la configuración, que sería como 
apagar y volver a encender el switch.
<p>Switch> enable 
<p>Switch# reload
<p>Al iniciar, comprobamos que los cambios en el switch no están (nombre del switch, 
direcciones IP, etc.).
<p>Volvemos a colocar el nombre al switch, y ahora grabaremos los cambios. Para realizar 
esta acción, debemos saber que un equipo CISCO posee dos ficheros de configuración: 
running‐config: almacena la configuración que está en ejecución en este momento. Es 
sobre la que hemos realizado los cambios hasta ahora. Este fichero, al iniciar el 
sistema, se sobre escribe con otro fichero: startup‐config.
startup‐config: como su nombre indica, es el fichero de configuración que se carga en 
el sistema al iniciar el mismo, y realiza una copia de si mismo sobre el fichero running‐ 
config.
<p>Con esta configuración, si en algún momento uno de los parámetros de configuración 
que tocamos provoca un comportamiento inadecuado, podemos solucionarlo 
volviendo a una configuración estable con solo reiniciar el switch.
<p>Para grabar la configuración, sólo debemos realizar una copia del fichero running‐ 
config sobre el fichero startup‐config. La forma de hacerlo no puede ser más clara: 
<p>Switch> enable
<p>Switch# copy running‐config startup‐config
Ahora, realizamos un cambio en el nombre del switch (Paso 2), copiamos la 
configuración y reiniciamos el switch. De esta forma comprobamos que nuestro equipo 
ha mantenido el cambio de nombre.
<p>También volveremos a realizar el paso 5 de colocar la IP, ya que la necesitamos en el 
paso siguiente, y grabaremos la configuración. Podemos comprobar que la IP funciona 
realizando un ping desde un equipo que esté enganchado al switch.
<p>Paso 7. Acceso mediante Telnet.
Además de tener configurada una dirección IP para nuestro switch, éste posee 5 
conexiones para telnet desde el exterior que pueden ser activadas. Lógicamente, al ser 
conexiones externas, se debe establecer una contraseña para dicha conexión. Estas 
acciones se realizan mediante lo comandos:
<p>Switch> enable
<p>Switch# configure terminal
<p>Switch# enable password cisco (debe tener contraseña el acceso al switch hasta 
por consola)
<p>Switch(config)# line vty 0 4 (accedemos a la configuración de los 5 interfaces telnet) 
<p>Switch(config‐line)# password cisco (colocamos la contraseña cisco para 
accede mediante telnet)
<p>Switch(config‐line)# login (activamos la petición de contraseña)
6
Ahora, procederemos a acceder desde un ordenador conectado a ese switch mediante 
la opción de Escritorio, entrando en el modo comando, e invocando el comando 
Telnet  
  
   
![Ejercicio 6](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20tracer%20PKT%201/Ejercicio%206.pkt "IMG")   
  
  
<h1>Ejercicio 7. Configuración de puertos.</h1>

<p>Durante el uso de un switch, y por problemas con los equipos o las tarjetas de red, 
puede ser interesante el poder gestionar los puertos sin tener que tocar los cables. 
Veamos los cambios más frecuentes que podemos realizar sobre un puerto.
<p>Paso 1. Auto‐negociación o fijado de velocidad.
Esta configuración la haremos utilizando el switch 2950T que posee dos puertos 
Gigabit. En el PC que utilicemos vamos a colocar, en lugar de la tarjeta estándar que 
viene, una tarjeta de par trenzado Gigabit. De esta forma tendremos una unión entre 
el switch y el PC a Gigabit.
<p>Veamos cual es la situación normal del puerto: 
Switch# show interfaces GigabitEthernet1/1 
Esto devuelve:
<p>De esta forma comprobamos la velocidad del puerto. 
Si queremos cambiarla, utilizamos los comandos: 
<p>Switch# configure terminal
<p>Switch(config)#interface gigabitEthernet1/1 
<p>Switch(config‐if)#speed 10

<p>Y comprobamos que, ahora, la velocidad de nuestro puerto a cambia a 10 Mbps.
<p>Switch# show interfaces GigabitEthernet1/1
Podemos hacer lo mismo colocando la velocidad a 100: 
<p>Switch(config)#interface gigabitEthernet1/1 
<p>Switch(config‐if)#speed 100
<p>O volviendo a colocar la velocidad en automático: 
<p>Switch(config)#interface gigabitEthernet1/1 
<p>Switch(config‐if)#speed auto
<p>Paso 2. Desactivar un puerto.
Hay momentos en que podremos necesitar el desactivar un puerto, ya sea porque la 
tarjeta de red del equipo no funciona correctamente, o por haber detectado que quien 
hace uso de ese puerto no está autorizado.
<p>Por este motivo, podemos desactivar un puerto.
Partiendo de la configuración anterior, podemos desactivar cualquier puerto del 
switch. Esta acción la conseguimos con los comandos:
<p>Switch>enable 
<p>Switch#configure terminal
<p>Switch(config)#interface gigabitEthernet1/1 
<p>Switch(config‐if)#shutdown
<p>Comprobar el funcionamiento de este comando mediante el añadido de varios equipos 
al switch a diferentes puertos
  
![Ejercicio 7](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20Tracer%20img%201/Practica%207.png "IMG")   
  
  
![Ejercicio 7](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20Tracer%20img%201/Practica%207%2C2.png "IMG")   
  
  
 ![Ejercicio 7](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20Tracer%20img%201/Practica%207%2C3.png "IMG")    
  
 ![Ejercicio 7](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20tracer%20PKT%201/Ejercicio%207.pkt "IMG")
  
  
  
  <h1> Parte Dos </h1>
  
<h1>Ejercicio 1. Inalámbrico. Red Abierta.</h1>
Realicemos una configuración de una red inalámbrica sin seguridad.
<p>Paso 1. Insertar un dispositivo inalámbrico Linksys WRT300N (Punto de acceso). Por 
defecto, este equipo viene con la configuración 192.168.0.1 y máscara de red 
255.255.255.0. Debemos colocar la configuración con la IP 192.168.1.1 y máscara de 
red 255.255.255.0. Además, debemos desactivar la asignación de direcciones 
mediante DHCP en el dispositivo inalámbrico.
<p>Paso 2. Insertar tres PC’s inalámbricos, con las siguientes configuraciones:
Nombre Dirección IP Máscara de red
<p>PC01 192.168.1.11 255.255.255.0
<p>PC02 192.168.1.12 255.255.255.0
<p>PC03 192.168.1.13 255.255.255.0
<p>Comprobar que el SSID de todos los equipos insertados es Default.
<p>Paso 3. Comprobar la comunicación entre los diferentes PC’s, y su comunicación con 
el punto de acceso. Observar esta comunicación en el modo simulación. ¿A qué te 
recuerda este tipo de propagación de tramas?
<p>Paso 4. Cambia la configuración de los equipos:
Nombre Dirección IP Máscara de red
<p>PC01 192.168.101.11 255.255.255.0
<p>PC02 192.168.101.12 255.255.255.0
<p>PC03 192.168.101.13 255.255.255.0
<p>Paso 5. Comprobar la comunicación entre los diferentes PC’s, y su comunicación con 
el punto de acceso. Como podemos comprobar, la configuración IP del punto de 
acceso no impide una correcta comunicación entre los diferentes PC’s que se conecten 
a su red.
  
#### ***Conclusiones***. <a name="id5"></a>

Las mayores dificultades fueron por parte de los switches a la hora de configurarlo
