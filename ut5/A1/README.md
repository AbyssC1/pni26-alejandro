<center>

<h1> UT5-A1 Comandos de red </h1>

</center>

***Nombre:Alejandro Hernandez***
***Curso:1º de Ciclo Superior de Administración de Sistemas Informáticos en Red*** 

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2) 
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

En el siguente apartado aprenderemos sobre los componentes que gestionan una red.

#### ***Objetivos***. <a name="id2"></a>

Aprender a conocer los comandos tanto en windows como en linux de una red.

#### ***Material empleado***. <a name="id3"></a>

Enumeramos el material empleado tanto hardware como software y las conficuraciones que hacemos (configuraciones de red por ejemplo) 

### Use el comando ipconfig /all para ver la dirección MAC de tu equipo. Y la siguiente aplicación
http://coffer.com/mac_find/ para rellenar la siguiente tabla

<center>

| Comandos a realizar                | Resultados                                       |
| -----------------------------------|--------------------------------------------------|  
| Dirección IP v4                    |  172.18.99.16                                    |
| Máscara                            |  255.255.0.0                                     |
| Gateway                            |  172.18.0.1                                      |
| MAC                                |  08-00-27-73-A7-53                               |
| Fabricante                         |  Intel(R) PRO/1000 MT Desktop Adapter            |
| Dirección IP v6                    |  00-01-00-01-29-8a-9e-33-08-00-27-73-a7-53       |
| Servidores DNS                     |  80.58.61.250                                    | 
| Tiempo de concesión de la IP       |  Martes, 1 de febrero de 2022 8:49:01            |
| Nombre del adaptador de red        |  Intel(R) PRO/1000 MT                            |

</center>

![alt text](https://github.com/AbyssC1/pni17-alejandro/blob/main/Imagenes/UT5/Windows/Para%20PNI%20comandos.png "IMG")

Liberar la configuración IP del adaptador con ipconfig /release y a continuación volver a usar el
comando ipconfig.

¿Cuál es la ip ahora?

<center>
  
<p> No hay ip ya que libera y renueva la dirección IP.  </p>                                                

</center>

![alt text](https://github.com/AbyssC1/pni17-alejandro/blob/main/Imagenes/UT5/Windows/Para%20PNI%20comandos%20release.png "IMG")

Ejecutar el comando ipconfig /renew solicitando una renovación de dirección IP. A continuación 
volver a ejecutar ipconfig. ¿Cuál es la nueva ip?


<p> solicita a un servidor de DHCP una nueva configuración IPv4 </p>

![alt text](https://github.com/AbyssC1/pni17-alejandro/blob/main/Imagenes/UT5/Windows/renew%20pni.png "IMG")

Ejecutar el comando ipconfig /displaydns y comprobar la información que contiene la caché DNS 
de  tu  equipo.  Ejecuta  ahora  el  comando  ipconfig  /flushdns y  después  muestra  otra  vez  el 
contenido de la caché DNS. ¿Qué información muestra ahora? ¿Qué ha ocurrido?

<p> Nos muestra los valores DNS que se están almacenados en la caché de nuestro sistema </p>

![alt text](https://github.com/AbyssC1/pni17-alejandro/blob/main/Imagenes/UT5/Windows/ipconfig%20displaydns%20y%20ipconfig%20flushdns.png "IMG")


Usar el navegador para ir a la web http://www.iespuertodelacruz.es y luego ejecutar el comando 
ipconfig /displaydns. Hacer una captura de pantalla donde se muestre que se ha cacheado la ip de 
ese nombre de dominio y pegarla aquí debajo.

<p> Vamos a la pagina </p>

![alt text](https://github.com/AbyssC1/pni17-alejandro/blob/main/Imagenes/UT5/Windows/displaydns%20con%20ies%20puerto%20de%20la%20cruz.png "IMG")


Borra la caché DNS con el comando ipconfig /flushdns y muestra una captura de pantalla en que 
se vea que ya no hay registros DNS en caché.

<p> Borramos la caché </p>

![alt text](https://github.com/AbyssC1/pni17-alejandro/blob/main/Imagenes/UT5/Windows/flushdns.png "IMG")

2.	Comando	ifconfig	(Línux)	
Este comando nos permite mostrar la configuración IP de nuestra máquina y configurar algunos 
parámetros. Algunas opciones de interés son:
Ifconfig  –a àNos muestra la configuración de todas las tarjetas de red incluso las desactivadas.
Ifconfig eth0 down àDesactiva una tarjeta de red llamada eth0. (También vale ifdown eth0)
Ifconfig eth0 up àActiva la tarjeta de red llamada eth1. (También vale ifup eth0)
Ifconfig eth0 192.168.1.1 netmask 255.255.255.192 à Asigna una IP y una máscara a la tarjeta 
eth0.

Ejercicios
Ejecuta el comando ifconfig y rellena lo que puedas de la siguiente tabla.

| Comandos a realizar                | Resultados                                       |
| ---------------------------------- | -------------------------------------------------|  
| Dirección IP v4                    | 192.168.1.40                                     |
| Máscara                            | 255.255.255.0                                    |
| Gateway                            | 192.168.1.1                                      |
| MAC                                | 80:00:27:bc:9f:f6                                |
| Fabricante                         | Intel(R) PRO/1000 MT Desktop Adapter             |
| Dirección IP v6                    | 00-01-00-01-30-8e-9e-33-08-00-27-73-a7-53        |
| Servidores DNS                     | 127.0.0.53                                       | 
| Tiempo de concesión de la IP       | jue feb 10 20:52:07 WET 2022                     |
| Nombre del adaptador de red        | Intel(R) PRO/1000                                |


Desactiva tu tarjeta de red con el comando ifconfig eth0 down. A continuación, comprueba con un 
ifconfig que la tarjeta ya no aparece, se ha desactivado. Haz una captura de pantalla donde se vea 
que ya no está activada.

<p> Quita el lo en mi caso </p>

![alt text](https://github.com/AbyssC1/pni17-alejandro/blob/main/Imagenes/UT5/Linux/1ifconfig%20verdadera.png "IMG")

Usa el comando ifconfig –a para ver que la tarjeta está desactivada, pero nadie la ha robado. Sigue 
ahí.
Ahora  activa  la  tarjeta  con  el  comando  ifconfig  eth0  up  y  luego  con  el  comando  ifconfig 
comprueba que ya está habilitada.
Usa  el  comando  ifconfig  eth0  192.168.99.99  netmask  255.255.255.0  y  pega  una  captura  de 
pantalla que muestre que el adaptador de red se ha configurado correctamente.

<p> Configura ifconfig  lo 192.168.99.99  netmask  255.255.255.0 </p>

![alt text](https://github.com/AbyssC1/pni17-alejandro/blob/main/Imagenes/UT5/Linux/2ifconfig%20lo%20down.png "IMG")

Usa el comando ifconfig eth0 IP netmask Máscara (con la configuración inicial de red) y pega una 
captura de pantalla que muestre que el adaptador de red se ha configurado correctamente.

<p> Comprobacion </p>

![alt text](https://github.com/AbyssC1/pni17-alejandro/blob/main/Imagenes/UT5/Linux/4lo%20configurado%20correctamente.png "IMG")

3.	Comando	ping	(Windows	y	Línux)	
Se usa para saber si hay comunicación entre equipos. Podría “no funcionar” en caso de que el 
ordenador al que hacemos el ping tenga un firewall que ignore nuestros mensajes. 
Algunas opciones para Windows/Linux son
-n àIndica el número de paquetes que se enviarán. (-c en linux) 
-l àestablece el tamaño del mensaje que se envía. (-s en linux)
-t àenvía paquetes de manera indefinida hasta que lo paramos con “ctrl+c”
-i à establecemos el TTL del ping, es decir, el número de saltos que debe dar antes de que lo 
destruyan. (-t en linux)


Ejercicios

Desde una máquina con línux ejecuta el comando ping –s 100 –c 2  ip_puertadeenlace para que se 
envíen dos ecos de 100 bytes. Muestra una captura de pantalla con el resultado.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG

Desde una máquina con windows usa el comando ping –i 2 ip_puertadeenlace para hacer un ping 
a nuestra puerta de enlace con un TTL igual a 2. 
Luego haz un ping de las mismas características, pero a google ping –i 2 www.google.es. Pega una 
captura de pantalla con el resultado y explica lo que ha pasado.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG


El comando ping nos da información sobre el tiempo de latencia de una red. Haz un ping a nuestra 
puerta de enlace y luego a otro a www.google.es. Busca información de lo que es el tiempo de 
latencia y compara los tiempos de latencia en ambos casos. 

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG


4.	Comando	route	(Línux)	
Nos permite ver y configurar la tabla de rutas de nuestro equipo. Algunas opciones de uso son:
Route àNos muestra la tabla de enrutamiento del equipo.
Route del default gw ip_gatewayàBorra la ruta por defecto. 
Route add default gw ip_gateway àAñade la puerta de enlace indicada para nuestro host.

Ejercicios

Usa el comando route para ver la puerta de enlace de tu equipo. ¿Cuál es tu puerta de enlace?

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG

Borra la puerta de enlace usando el comando Route del default gw ip_gateway. A continuación, 
ejecuta el comando route para comprobar que ya no hay puerta de enlace. Intenta navegar por 
internet y verás que tampoco puedes. Haz una captura de pantalla con la salida del comando 
route y del resultado de ping 8.8.8.8 ¿Cómo interpretas el mensaje que te devuelve el ping?

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG

Vuelve a configurar la puerta de enlace usando el comando route add default gw ip_gateway y 
comprueba que ya ha vuelto la puerta de enlace con el comando route.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG

5.	Comando	netstat	(Línux	y	Windows)	
Nos muestra las conexiones que tiene nuestro host abiertas con la red. Algunas opciones para 
linux son:
-t → Muestra las conexiones tcp abiertas. (en windows -p tcp) 
-u → Muestra las conexiones udp abiertas. en windows -p udp)
-a → Muestra los puertos que estén esperando conexiones (puertos en escucha). 
-n → Para que muestre solo información numérica.
-s → Nos muestra estadísticas sobre nuestra conexión de red. 
-r → Nos muestra la tabla de enrutamiento de nuestro host.

Ejercicios

Abre una página web cualquiera y luego ejecuta el comando netstat -t para que nos muestre las 
conexiones que tenemos abiertas por tcp. Pon una captura de pantalla del resultado y explica lo 
que es cada una de las columnas que aparecen.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG

Ahora espera unos segundos y vuelve a ejecutar netstat -tn. Comprobarás que algunas de las 
conexiones se han cerrado o están esperando para cerrarse. Además con la opción -n verás los resultados  en  formato  numérico.  Pon  una  captura  de  pantalla  y  explica  la  diferencia  entre 
Established, Time_wait y Close_Wait.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG

Ejecuta ahora la orden netstat -at para que muestre las tanto las conexiones tcp abiertas como los 
puertos que están a la escucha. Copia una captura de pantalla donde se vean los puertos que 
tienes  escuchando,  explica  qué    significan  los  asteriscos  en  la  columna  “Foreign  address”  e 
investiga si tener esos puertos abiertos es normal o supone una amenaza.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG

Ejecuta el comando netstat -s para ver las estadísticas de red  y haz una captura en la que se vean 
cuantos paquetes tcp has recibido y cuantos de ellos han sido erroneos.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG


6.	Comando	arp	(Línux	y	Windows)
Se usa para mostrar y administrar la caché ARP de nuestro equipo. Las opciones más habituales 
son:
Arp -a → Muestra la tabla arp del host (en línux no hace falta el -a)
arp -d dirección_ip → borra de la tabla la entrada indicada
arp -d * → borra toda la tabla arp (el equivalente en linux: ip neigh flush all)
arp -s direccion_ip  direccion_mac → crea una entrada en la tabla ARP

Ejercicio

Borra toda la caché ARP con el comando arp -d *. A continuación haz un ping a la puerta de 
enlace. Pon una captura de la tabla ARP en que se vea que solo está la puerta de enlace y su mac.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG

Ahora  borra  manualmente  la  entrada  arp  de  la  puerta  de  enlace  con  la  orden  arp -d 
ip_puertadeenlace. Luego introduce manualmente una mac falsa para la puerta de enlace en la 
tabla arp con el comando arp -s ip_puertadeenlace aa:bb:cc:dd:ee:ff Haz una captura de pantalla 
en que se vea el resultado del comando arp -a y de hacer un ping a google. Explica por qué ahora 
no hay internet.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG

Borra la entrada falsa de la tabla arp con el comando arp -d ip_puertadeenlace.


7.	Comando	nslookup	(Windows	y	Linux)
Este  comando  nos  da  información  sobre  la  resolución  de  nombres  dns.  Nos  dice  a  quién  le 
hacemos la consulta y qué respuesta nos da. Opciones principales:
nslookup dominio → Consulta a nuestro servidor dns por el dominio indicado. 
Nslookup dominio ip_servidordns → consulta al servidor dns indicado por el dominio.

Ejercicios

Averigua el nombre del servidor DNS de www.iespuertodelacruz.es. A continuación, ejecutamos 
el comando nslookup nombreServidorDNS y luego el comando nslookup nombreServidorDNS
8.8.8.8. Explica las causas de las diferencias que hay entre los resultados de las dos consultas.

|---------------------------------------------------------------------------------------------------------------------------------|
| Renovamos la IP. |

IMG


#### ***Conclusiones***. <a name="id5"></a>

Los comandos realizados en esta practica son importantes para aprender mas sobre las redes y direccionamientos de IP.
