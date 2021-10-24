<h1> UT3-A1 Ejercicios modelo OSI </h1>

1.¿Qué niveles OSI son los niveles de soporte de red? 

<p> Nivel 1: Físico 
<br>Nivel 2: Enlace 
<br>Nivel 3: Red 

2.¿Qué niveles OSI son los niveles de soporte de usuario? 
  
<p> Nivel 5: Sesión
<br>Nivel 6: Presentación
<br>Nivel 7: Aplicación

3.¿Cómo están OSI e ISO relacionadas entre sí?
  
<p>Están relacionados porque ISO es la organización de estándares 
que creo el modelo de interconexión de sistemas abiertos OSI.</p> 

4.Enumere los niveles del modelo OSI.

<p>Nivel 1: Físico 
<br>Nivel 2: Enlace 
<br>Nivel 3: Red 
<br>Nivel 4: Transporte 
<br>Nivel 5: Sesión 
<br>Nivel 6: Presentación 
<br>Nivel 7: Aplicación

5.¿Cómo pasa la información de un nivel OSI al siguiente? 
  
<p>Pasa del nivel mas alto (7) en la maquina A hasta el nivel mas 
bajo (1) de la misma, y se envía en lujo de bits al nivel mas bajo 
(1) de la maquina B y sube hasta el nivel mas alto (7) de la 
maquina B.
  
6.¿Qué son las cabeceras y cola y cómo se añaden y se quitan?
  
<p>-Las cabeceras o colas son datos de control que se añaden al 
principio o al final de un paquete de datos. 
<br>-Las cabeceras se añaden en la maquina emisora en los niveles, 
6 , 5 , 4, 3, 2, y en el nivel 2 se añade una cola.
<br>-Se quitan en la maquina receptora al pasar nivel por nivel, cada 
nivel procesa y elimina los datos que son para el.
 
7.¿Cuáles son las responsabilidades del nivel físico? 
  
<p>-Características físicas de las interfases y el medio. 
<br>-Representación de los bits 
<br>-Tasa de datos 
<br>-Sincronización de los bits 
<br>-Coniguración de la línea 
<br>-Topología física 
<br>-Modos de transmisión  
  
8.¿Cuáles son las responsabilidades del nivel de enlace? 
  
<p>-Tramado 
<br>-Direccionamiento físico 
<br>-Control de lujo 
<br>-Control de errores 
<br>-Control de acceso

9.¿Cuáles son las responsabilidades del nivel de red? 
 
<p>-Direccionamiento lógico 
<br>-Encaminamiento

10.¿Cuáles son las responsabilidades del nivel de transporte? 
  
<p>-Direccionamiento en punto de servicio. 
<br>-Segmentación y reensamblado. 
<br>-Control de conexión 
<br>-Control de lujo 
<br>-Control de errores
  
11.El nivel de transporte crea una conexión entre el origen y el destino. ¿Cuáles son los tres eventos involucrados en la conexión? 
  
<p>-Establecimiento de la conexión 
<br>-Transferencia de datos 
<br>-Liberación de la conexión

12.¿Cuál es la diferencia entre una dirección de punto en servicio, una dirección lógica y una dirección fisica? 
  
<p>Direccionamiento lógico: el direccionamiento físico 
proporcionado por el nivel de enlace de datos gestiona los 
problemas de direcciones locales si un paquete cruza la frontera 
de la red es necesario tener otro tipo de direcciones para 
distinguir los sistemas origen de los del destino, el nivel de red 
añade una cabecera al paquete que viene del nivel superior que 
entre otras cosas incluye las direcciones lógicas del emisor y el 
receptor.
  
<p>Punto de servicio: las computadoras suelen ejecutar a 
menudo varios programas al mismo tiempo por esa razón la 
entrega desde el origen al destino signiica la entrega no solo de 
una pc a otra sino también desde un proceso especiico 
(programa de ejecución) en una pc a un proceso especiico en el 
otro.
  
<p>Direccionamiento físico: si es necesario distribuir las tramas 
por distintos sistemas de la red, el nivel de enlace de datos 
añade una cabecera a la trama para deinir la dirección física del
emisor (dirección fuente) y/o receptor (dirección destino) de la 
trama. Si hay que enviar la trama a un sistema fuera de la red 
del emisor, la dirección de receptor es la dirección de dispositivo
que conecta su red a la siguiente.
  
13.¿Cuáles son las responsabilidades del nivel de sesión?
  
<p>-Control de dialogo 
<br>-Sincronización 
  
14.¿Cuáles son las responsabilidades del nivel de presentación? 
  
<p>-Traducción 
<br>-Cifrado 
<br>-Compresión  
  
15.¿Cuál es el objetivo de la traducción en el nivel de presentación? 

<p>Traducir la información a lujos de bits antes de transmitirla, 
debido a que cada computadora usa un sistema de codiicación 
distinto.
  
16.Indique alguno de los servicios proporcionados por el nivel de aplicación. 
  
<p>Algunos de los servicios son:

<p>-Servicios de terminal remoto (Telnet)
<br>-Servicios de correo
<br>-Servicios de transferencia de ficheros (ftp)
<br>-Servicios web
<br>-Servicios DNS
<br>-Servicios DHCP

  
17.¿Cómo se relacionan los niveles de la familia del protocolo TCP/IP con los niveles del modelo OSI?

18.El nivel<p style="color:#FF0000";>Sesión</p>decide la localización de los puntos de sincronización. 
transporte
sesión
presentación
aplicación

19. En el nivel _______________, la unidad de datos se denomina trama.

físico
enlace de datos
red
transporte
  
20. Los servicios de correo y de directorio están disponibles a los usuarios de la red a través del nivel:

enlace de datos
sesión
transporte
aplicación
  
21. A medida que los paquetes de datos se mueven  de los niveles inferiores a los superiores las cabeceras:

añadidas
eliminadas
recolocadas
modificadas
