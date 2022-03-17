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
SW01 2 SW02 1
SW01 3 SW03 1
SW02 4 SW04 2
<p>Paso 3. Insertar los siguientes equipos con sus correspondientes configuraciones:
Nombre IP Máscara Switch Puerto
PC01 10.0.1.101 255.255.0.0 SW01 11
PC02 10.0.2.102 255.255.0.0 SW02 12
PC03 10.0.3.103 255.255.0.0 SW03 13
PC04 10.0.4.104 255.255.0.0 SW04 14
<p>Paso 4. Comprobar la conectividad de los 4 equipos.
<p>Paso 5. Introducir una nueva conexión entre switchs entre el SW01 puerto 4 y el 
SW04 puerto 1. Esto crea un circuito entre los equipos. Comprobar qué sucede con la 
comunicación entre equipos.
<p>Paso 6. Eliminar la última conexión realizada. Añadir un Generic Hub‐PT y 
denominarlo HUB05. Utilizando el puerto 1 de este hub, unirlo al SW04 puerto 1. 
Insertar un nuevo equipo con la configuración PC05, 10.0.5.105, 255.255.0.0, al puerto 
del hub número 5. Comprobar la conectividad de los 4 equipos anteriores con éste
  
 ![Ejercicio 4](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20Tracer%20img%201/Ejercicio%204.png "IMG")
  <p>
 ![Ejercicio 4](https://github.com/AbyssC1/pni26-alejandro/blob/main/ut5/A5/Packet%20tracer%20PKT%201/Ejercicio%204.pkt "IMG")
  
  
  
  
  
#### ***Conclusiones***. <a name="id5"></a>

Las mayores dificultades fueron por parte de los switches a la hora de configurarlo