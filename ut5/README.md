UT5-A1 Comandos de red. 
 
Objetivo 
La siguiente práctica está destinada a aprender, comprender algunos comandos importantes que
son de gran utilidad en la administración de una red. Tan importantes o más que saber atarse los
zapatos.

Material necesario 
Necesitaremos dos máquinas virtuales o reales. Una con un sistema operativo Windows y otra con
Linux.

1. Comando ipconfig (Windows) 
Este comando nos permite ver datos relacionados con la configuración de red de nuestro equipo.
Algunas de sus principales opciones son:
Ipconfig /all à Nos muestra información más detallada del adaptador de red.
Ipconfig /release à Libera las configuración asignada por dhcp.
Ipconfig /renew à Solicita al servidor DHCP la renovación de una configuración de red.
Ipconfig /displaydns à Muestra el contenido de la caché DNS de nuestro equipo.
Ipconfig /flushdns à Borra la caché DNS de nuestro equipo.
Ejercicios
Use el comando ipconfig /all para ver la dirección MAC de tu equipo. Y la siguiente aplicación
http://coffer.com/mac_find/ para rellenar la siguiente tabla.
Dirección IP v4
Máscara
Gateway
MAC
Fabricante
Dirección IP v6
Servidores DNS
Tiempo de concesión de la IP
Nombre del adaptador de red
Liberar la configuración IP del adaptador con ipconfig /release y a continuación volver a usar el
comando ipconfig.
¿Cuál es la ip ahora?
Ejecutar el comando ipconfig /renew solicitando una renovación de dirección IP. A continuación
volver a ejecutar ipconfig. ¿Cuál es la nueva ip?
Ejecutar el comando ipconfig /displaydns y comprobar la información que contiene la caché DNS
de tu equipo. Ejecuta ahora el comando ipconfig /flushdns y después muestra otra vez el
contenido de la caché DNS. ¿Qué información muestra ahora? ¿Qué ha ocurrido?
Usar el navegador para ir a la web http://www.iespuertodelacruz.es y luego ejecutar el comando
ipconfig /displaydns. Hacer una captura de pantalla donde se muestre que se ha cacheado la ip de
ese nombre de dominio y pegarla aquí debajo.
Borra la caché DNS con el comando ipconfig /flushdns y muestra una captura de pantalla en que
se vea que ya no hay registros DNS en caché.
2. Comando ifconfig (Línux) 
Este comando nos permite mostrar la configuración IP de nuestra máquina y configurar algunos
parámetros. Algunas opciones de interés son:
Ifconfig –a à Nos muestra la configuración de todas las tarjetas de red incluso las desactivadas.
Ifconfig eth0 down à Desactiva una tarjeta de red llamada eth0. (También vale ifdown eth0)
Ifconfig eth0 up à Activa la tarjeta de red llamada eth1. (También vale ifup eth0)
Ifconfig eth0 192.168.1.1 netmask 255.255.255.192 à Asigna una IP y una máscara a la tarjeta
eth0.
Ejercicios
Ejecuta el comando ifconfig y rellena lo que puedas de la siguiente tabla.
Dirección IP v4
Máscara
Gateway
MAC
Fabricante
Dirección IP v6
Servidores DNS
Tiempo de concesión de la IP
Nombre del adaptador de red
Desactiva tu tarjeta de red con el comando ifconfig eth0 down. A continuación, comprueba con un
ifconfig que la tarjeta ya no aparece, se ha desactivado. Haz una captura de pantalla donde se vea
que ya no está activada.
Usa el comando ifconfig –a para ver que la tarjeta está desactivada, pero nadie la ha robado. Sigue
ahí.
Ahora activa la tarjeta con el comando ifconfig eth0 up y luego con el comando ifconfig
comprueba que ya está habilitada.
Usa el comando ifconfig eth0 192.168.99.99 netmask 255.255.255.0 y pega una captura de
pantalla que muestre que el adaptador de red se ha configurado correctamente.
Usa el comando ifconfig eth0 IP netmask Máscara (con la configuración inicial de red) y pega una
captura de pantalla que muestre que el adaptador de red se ha configurado correctamente.
3. Comando ping (Windows y Línux) 
Se usa para saber si hay comunicación entre equipos. Podría “no funcionar” en caso de que el
ordenador al que hacemos el ping tenga un firewall que ignore nuestros mensajes.
Algunas opciones para Windows/Linux son
-n à Indica el número de paquetes que se enviarán. (-c en linux)
-l à establece el tamaño del mensaje que se envía. (-s en linux)
-t à envía paquetes de manera indefinida hasta que lo paramos con “ctrl+c”
-i à establecemos el TTL del ping, es decir, el número de saltos que debe dar antes de que lo
destruyan. (-t en linux)
Ejercicios
Desde una máquina con línux ejecuta el comando ping –s 100 –c 2 ip_puertadeenlace para que se
envíen dos ecos de 100 bytes. Muestra una captura de pantalla con el resultado.
Desde una máquina con windows usa el comando ping –i 2 ip_puertadeenlace para hacer un ping
a nuestra puerta de enlace con un TTL igual a 2.
Luego haz un ping de las mismas características, pero a google ping –i 2 www.google.es. Pega una
captura de pantalla con el resultado y explica lo que ha pasado.
El comando ping nos da información sobre el tiempo de latencia de una red. Haz un ping a nuestra
puerta de enlace y luego a otro a www.google.es. Busca información de lo que es el tiempo de
latencia y compara los tiempos de latencia en ambos casos.
 
 
4. Comando route (Línux) 
Nos permite ver y configurar la tabla de rutas de nuestro equipo. Algunas opciones de uso son:
Route à Nos muestra la tabla de enrutamiento del equipo.
Route del default gw ip_gatewayà Borra la ruta por defecto.
Route add default gw ip_gateway à Añade la puerta de enlace indicada para nuestro host.
Ejercicios
Usa el comando route para ver la puerta de enlace de tu equipo. ¿Cuál es tu puerta de enlace?
Borra la puerta de enlace usando el comando Route del default gw ip_gateway. A continuación,
ejecuta el comando route para comprobar que ya no hay puerta de enlace. Intenta navegar por
internet y verás que tampoco puedes. Haz una captura de pantalla con la salida del comando
route y del resultado de ping 8.8.8.8 ¿Cómo interpretas el mensaje que te devuelve el ping?
Vuelve a configurar la puerta de enlace usando el comando route add default gw ip_gateway y
comprueba que ya ha vuelto la puerta de enlace con el comando route.
5. Comando netstat (Línux y Windows) 
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
Ahora espera unos segundos y vuelve a ejecutar netstat -tn. Comprobarás que algunas de las
conexiones se han cerrado o están esperando para cerrarse. Además con la opción -n verás los
resultados en formato numérico. Pon una captura de pantalla y explica la diferencia entre
Established, Time_wait y Close_Wait.
Ejecuta ahora la orden netstat -at para que muestre las tanto las conexiones tcp abiertas como los
puertos que están a la escucha. Copia una captura de pantalla donde se vean los puertos que
tienes escuchando, explica qué significan los asteriscos en la columna “Foreign address” e
investiga si tener esos puertos abiertos es normal o supone una amenaza.
Ejecuta el comando netstat -s para ver las estadísticas de red y haz una captura en la que se vean
cuantos paquetes tcp has recibido y cuantos de ellos han sido erroneos.
6. Comando arp (Línux y Windows)
Se usa para mostrar y administrar la caché ARP de nuestro equipo. Las opciones más habituales
son:
Arp -a → Muestra la tabla arp del host (en línux no hace falta el -a)
arp -d dirección_ip → borra de la tabla la entrada indicada
arp -d * → borra toda la tabla arp (el equivalente en linux: ip neigh flush all)
arp -s direccion_ip direccion_mac → crea una entrada en la tabla ARP
Ejercicio
Borra toda la caché ARP con el comando arp -d *. A continuación haz un ping a la puerta de
enlace. Pon una captura de la tabla ARP en que se vea que solo está la puerta de enlace y su mac.
Ahora borra manualmente la entrada arp de la puerta de enlace con la orden arp -d
ip_puertadeenlace. Luego introduce manualmente una mac falsa para la puerta de enlace en la
tabla arp con el comando arp -s ip_puertadeenlace aa:bb:cc:dd:ee:ff Haz una captura de pantalla
en que se vea el resultado del comando arp -a y de hacer un ping a google. Explica por qué ahora
no hay internet.
Borra la entrada falsa de la tabla arp con el comando arp -d ip_puertadeenlace.

7. Comando nslookup (Windows y Linux)
Este comando nos da información sobre la resolución de nombres dns. Nos dice a quién le
hacemos la consulta y qué respuesta nos da. Opciones principales:
nslookup dominio → Consulta a nuestro servidor dns por el dominio indicado.
Nslookup dominio ip_servidordns → consulta al servidor dns indicado por el dominio.

Ejercicios
Averigua el nombre del servidor DNS de www.iespuertodelacruz.es. A continuación, ejecutamos
el comando nslookup nombreServidorDNS y luego el comando nslookup nombreServidorDNS
8.8.8.8. Explica las causas de las diferencias que hay entre los resultados de las dos consultas.
