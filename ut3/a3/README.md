1. Convierte las siguientes direcciones a binario e indica si se trata de direcciones de tipo A, B o C. 

    + `10.0.3.2`     00001010.00000000.00000011.00000010 Clase A
    + `128.45.7.1`   10000000.00101101.00000111.00000001 Clase B
    + `192.200.5.4`  11000000.11001000.00000101.00000100 Clase C
    + `151.23.32.50` 10010111.00010111.00100000.00110010 Clase B
    + `47.50.3.2`    00101111.00110010.00000011.00000010 Clase A
    + `100.90.80.70` 00000100.01011010.01010000.01000110 Clase A
    + `124.45.6.1`   01111100.00101101.00000110.00000001 Clase A

2. Dada la dirección de red `192.168.30.0`, indica qué máscara de subred deberías escoger para tener 4 subredes. Rellena a continuación la siguiente tabla. 

<center>

|           Número de red           | Dirección de subred | Primer host  | Último host    |
|-----------------------------------|---------------------|--------------|----------------|
|1                                  |  192.168.30.0       |192.168.30.1  |192.168.30.62   |
|2                                  |  192.168.30.64      |192.168.30.65 |192.168.30.126  |
|3                                  |  192.168.30.128     |192.168.30.129|192.168.30.190  |
|4                                  |  192.168.30.192     |192.168.30.193|192.168.30.254  |


</center>

3. Dada la dirección de red `192.168.55.0`, indica qué máscara de subred deberías escoger para tener 8 subredes. Rellena a continuación la siguiente tabla.

<center>

|         Número de red               | Dirección de subred | Primer host  | Último host  |
|-------------------------------------|---------------------|--------------|--------------|
|1                                    | 192.168.55.0        |192.168.55.1  |192.168.55.30 |
|2                                    | 192.168.55.32       |192.168.55.33 |192.168.55.62 |             
|3                                    | 192.168.55.64       |192.168.55.65 |192.168.55.94 |             
|4                                    | 192.168.55.96       |192.168.55.97 |192.168.55.126|             
|5                                    | 192.168.55.128      |192.168.55.129|192.168.55.158|
|6                                    | 192.168.55.160      |192.168.55.161|192.168.55.190|
|7                                    | 192.168.55.192      |192.168.55.193|192.168.55.222|
|8                                    | 192.168.55.224      |192.168.55.224|192.168.55.254|

</center>


4. Dada la dirección de clase B `150.40.0.0`, indica qué máscara de subred deberías escoger para tener 4 subred. Rellena a continuación la siguiente tabla.

<center>


| Número de red                       | Dirección de subred | Primer host | Último host  |
|-------------------------------------|---------------------|-------------|--------------|
|1                                    |150.40.0.0           |150.40.0.1   |150.40.63.254 |
|2                                    |150.40.64.0          |150.40.64.1  |150.40.127.254|
|3                                    |150.40.128.0         |150.40.128.1 |150.40.191.254|
|4                                    |150.40.192.0         |150.40.192.1 |150.40.255.254|

</center>


5. ¿Cuál es el intervalo decimal y binario del primer octeto para todas las direcciones `ip` clase "B" posibles?
<p>    10000000=128
<br>   10111111=191
<br>   El intervalo decimal es 128 - 191
<p>¿Qué octeto u octetos representan la parte que corresponde a la red de una dirección `ip` clase "C"?
<p> Los tres primero octetos.
<p>¿Qué octeto u octetos representan la parte que corresponde al host de una dirección `ip` clase "A"?
<p> Los tres ultimos octetos.

6. Completa la siguiente tabla:

<center>


| Dirección `ip` del host | Dirección clase | Dirección de red | Dirección de host | Dirección de broadcast de red | Máscara de subred por defecto |
|-------------------------|-----------------|------------------|-------------------|-------------------------------|-------------------------------|
| 216.14.55.137           |        C        |   216.14.55.0    |  216.14.55.137    |   216.14.55.255               |   255.255.255.0               |
| 123.1.1.15              |        A        |   123.0.0.0      |  123.1.1.15       |   123.255.255.255             |   255.0.0.0                   |
| 150.127.221.224         |        B        |   150.127.0.0    |  150.127.221.224  |   150.127.255.255             |   255.255.0.0                 |
| 194.125.35.199          |        C        |   194.125.35.0   |  194.125.35.199   |   194.125.35.255              |   255.255.255.0               |
| 175.12.239.244          |        B        |   175.12.0.0     |  175.12.239.244   |   175.12.255.255              |   255.255.0.0                 |

</center>

7. Dada una dirección `142.226.0.15` :

    + ¿Cuál es el equivalente binario del segundo octeto?
    + - 11100010
    + ¿Cuál es la Clase de la dirección?
    + - Clase B 
    + ¿Cuál es la dirección de red de esta dirección `ip`?
    + - 142.226.0.0
    + ¿Es ésta una dirección de host válida? ¿Por qué? o ¿Por qué no?
    + - Si por que no es una dirección de red ni de difusión privada.
    + ¿Cuál es la cantidad máxima de hosts que se pueden tener con una dirección de red de clase C? 
    + - 254 host como maximo.
    + ¿Cuántas redes de clase B puede haber?
    + - Dos elevado a las 16= 65536 redes
    + ¿Cuántos hosts puede tener cada red de clase B?
    + - Dos elevados a las 16 menos 2
    + ¿Cuántos octetos hay en una dirección `ip`?
    + - Cuatro octetos hay en una direccion ip
    + ¿Cuántos bits puede haber por octeto?
    + - Ocho bits

8. Determinar, para las siguientes direcciones de host `ip`, cuáles son las direcciones que son válidas para redes comerciales. Válida significa que se puede asignar a una estación de trabajo, servidor, impresora, interfaz de router, etc.

<center>

| Dirección `ip`  | ¿La dirección es válida? |                              ¿Por qué?                                                 |
|-----------------|--------------------------|----------------------------------------------------------------------------------------|
| 150.100.255.255 |           No             |  Es una direccion de difusión de una red de clase B                                    |
| 175.100.255.18  |           Si             |  No es un dirección de red ni de difusión                                              |
| 100.0.0.23      |           Si             |  No es un dirección de red ni de difusión                                              |
| 188.258.221.176 |           No             |  No por que tiene en el segundo octeto 258                                             |
| 127.34.25.189   |           No             |  Esta es una red de clase A pero no es valida por que comienza en 127 el primer octeto |                                           
| 224.156.217.73  |           No             |  Estan reservadas por que es una clases D                                              |

</center>


9. Completa la siguiente tabla:

<center>


|  ip           | Máscara        | Subred      | Broadcast     |
|---------------|----------------|-------------|---------------|
| 192.168.1.130 | 255.255.255.128|192.168.1.128|192.168.1.255  |
| 10.1.1.3      | 255.255.0.0    |10.1.0.0     |10.1.255.255   |
| 10.1.1.8      | 255.255.0.0    |10.1.0.0     |10.1.255.255   |
| 200.1.1.23    | 255.0.0.0      |220.0.0.0    |220.255.255.255|
| 172.168.8.48  | 255.255.248.0  |172.168.8.0  |172.168.15.255 |
| 172.16.8.48   | 255.255.255.224|172.16.8.32  |172.16.8.63    |

</center>

10. Asignar direcciones `ip` válidas a las interfaces de red (interfaz de red = tarjeta de red) que les falte para conseguir que exista comunicación entre los host A, B, C, D, E y F. La máscara en todos los casos será `255.255.224.0`. Justifica la respuesta.

<center>
    
| Direccion subred | Primer host | Ultimo host   |
|------------------|-------------|---------------|
|   172.33.32.0    |  172.33.32.1|  172.33.64.254|

</center>

<center>

![](img/001.png)

</center>

11. Tu empresa tiene una dirección de red de Clase C de `200.10.57.0` .Desea subdividir la red física en 3 subredes.
   <p> ¿Cuál es la dirección de red y la dirección de broadcast de cada una de las 3 subredes creadas?
<center>
    
| Dirección subred |   Primer host  | 
|------------------|----------------|
|   200.10.57.0    |   200.10.57.63 |
|   200.10.57.64   |   200.10.57.127|
|   200.10.57.128  |   200.10.57.191|
    
</center>
  
    + Indica una máscara que permita dividir la red de clase C (al menos) en tres subredes 
    + 255.255.255.192
    + ¿Cuántos hosts (ordenadores) puede haber por subred?
    + Si se cogen 2 bits para la mascara quedan 6 bits para asignar direcciones a los ordenadores
    
    

12. Se desea subdividir la dirección de red de clase C de `200.10.57.0` en 4 subredes. Responde a las siguientes preguntas:

    + ¿Cuál es el equivalente en números binarios de la dirección de red de clase C `200.10.57.0` de este ejercicio?
    + - 11001000.00001010.00111001.00000000
    + ¿Cuál(es) es (son) el (los) octeto(s) que representa(n) la porción de red y cuál(es) es (son) el (los) octeto(s) que representa(n) la porción de host de esta dirección de red de clase C?
    + - Los octetos que representan a la red son los 3 primeros. El octeto que representa al host es el último.
    + ¿Cuántos bits se deben pedir prestados a la porción de host de la dirección de red para poder suministrar 8 subredes?
    + - Se deben pedir prestados 3 bits para tener 8 subredes.   
    + ¿Cuál será la máscara de subred (utilizando la notación decimal) basándose en la cantidad de bits que se pidieron prestados en el paso 3?
    + - 255.255.255.224
    + ¿Cuál es el equivalente en números binarios de la máscara de subred a la que se hace referencia anteriormente?
    + - 11111111.11111111.11111111.11100000
       
13. Teniendo en cuenta la dirección `ip` del ejercicio anterior (`200.10.57.0`) completa la siguiente tabla para cada una de las posibles subredes que se pueden crear pidiendo prestados 3 bits para subredes al cuarto octeto (octeto de host). Identifica la dirección de red, la máscara de subred, el intervalo de direcciones `ip` de host posibles para cada subred, la dirección de broadcast para cada subred.

<center>


|  Subred | Dirección de subred | Primer host      | Último host      |
|---------|---------------------|------------------|------------------|
| 1       | 200.10.57.0         |200.10.57.1       |200.10.57.30      |
| 2       | 200.10.57.32        |200.10.57.33      |200.10.57.62      |
| 3       | 200.10.57.64        |200.10.57.65      |200.10.57.94      |
| 4       | 200.10.57.96        |200.10.57.97      |200.10.57.126     |
| 5       | 200.10.57.128       |200.10.57.129     |200.10.57.158     |
| 6       | 200.10.57.160       |200.10.57.161     |200.10.57.190     |
| 7       | 200.10.57.192       |200.10.57.193     |200.10.57.222     |
| 8       | 200.10.57.224       |200.10.57.225     |200.10.57.254     |

</center>


14. Completa la siguiente tabla:

<center>


| `ip`          | Máscara         | Subred        | Broadcast     | Número hosts |
|---------------|-----------------|---------------|---------------|--------------|
| 192.168.1.130 | 255.255.255.128 | 192.168.1.128 | 192.168.1.255 | 126          |
| 200.1.17.15   | 255.255.255.0   | 200.1.17.0    | 200.1.17.255  | 254          |
| 133.32.4.61   | 255.255.255.224 | 133.32.4.32   | 133.32.4.63   | 30           |
| 132.4.60.99   | 255.255.0.0     | 132.4.0.0     | 132.4.255.255 | 65534        |
| 222.43.15.41  | 255.255.255.0   | 222.43.15.0   | 222.43.15.255 | 2 a la 6 -2  |
| 192.168.0.1   | 255.255.255.192 | 192.168.0.0   | 192.168.0.63  | 30           |

</center>

15. Responde a las siguientes preguntas:

    + Si tenemos una red `147.84.32.0` con máscara de red `255.255.255.252`, indica la dirección de broadcast, la de red y la de los posibles nodos de la red.
    + -  Dirección de red: 147.84.32.0
        <br> Broadcast: 147.84.32.3
        <br> Posibles Nodos: 147.84.32.1, 147.84.32.2
    + La red `192.168.0.0`, ¿de qué clase es?
    + - Clase C
    + Escribe el rango de direcciones `ip` que pertenecen a la subred definida por la dirección `140.220.15.245` con máscara `255.255.255.240`.
    + - Primero hay que calcular la subred a la que pertenece la IP 
        140.220.15.245 = 255.255.255.240 = 140.220.15.240
        <p>10001100.11011100.00001111.11110101       
        <br>11111111.11111111.11111111.11110000     
        <br>10001100.11011100.00001111.11110000 
        <p>La subred a la que pertenece la IP 140.220.15.245 es 140.220.15.240 
        El primer ordenador de la subred es 140.220.15.241 
        La dirección de difusión de la subred es 10001100.11011100.00001111.1111 1111 = 140.220.15.255 
        Por tanto, la dirección del último ordenador de la subred es 140.220.15.254 
    + Una red de clase B en Internet tiene una máscara de subred igual a `255.255.240.0`. ¿Cuál es el máximo de nodos por subred?
    + - Al ser el tercer octecto de la subred 240, quiere decir que se toman prestados 4 bits de la máscara. Hay por tanto 8+4=12 bits que identifican un ordenador dentro de la         red. Por tanto el número máximo de ordenadores dentro de cada subred será 212-2. 

16. Calcular la dirección de red y la dirección de broadcast (difusión) de las máquinas con las siguientes direcciones IP y máscaras de subred (si no se especifica, se utiliza la máscara por defecto).

    + `18.120.16.250`                         Dirección de red: 18.0.0.0       Broadcast: 18.255.255.255
    + `18.120.16.255 / 255.255.0.0`           Dirección de red: 18.120.0.0     Broadcast: 18.120.255.255
    + `155.4.220.39`                          Dirección de red: 155.4.0.0      Broadcast: 155.4.255.255
    + `194.209.14.33`                         Dirección de red: 194.209.14.0   Broadcast: 194.209.14.255
    + `190.33.109.133 / 255.255.255.0`        Dirección de red: 190.33.109.0   Broadcast: 190.33.109.255
    + `190.33.109.133 / 255.255.255.128`      Dirección de red: 190.33.109.128 Broadcast: 190.33.109.255
    + `192.168.20.25 / 255.255.255.240`       Dirección de red: 192.168.20.16  Broadcast: 192.168.20.31
    + `192.168.20.25 / 255.255.255.192`       Dirección de red: 192.168.20.0   Broadcast: 192.168.20.63

17. Responde a las siguientes preguntas:

    + ¿Cuántos ordenadores como máximo se pueden tener en una red de clase A?
    + - 2 a la 24 -2        
    + ¿Cuántos ordenadores como máximo se pueden tener en una red de clase B?
    + - 2 a la 16 -2       
    + ¿Cuántos ordenadores como máximo se pueden tener en una red de clase C?
    + - 2 a la 8 -2        
    + En una red de clase C con máscara `255.255.255.128`, ¿cuántos ordenadores se pueden tener en cada subred?
    + - Como se toma prestado un bit de la máscara quedarian 7 bits para identificar un ordenador dentro de cada subred. Con 7 bits hay 2 a la 7 de combinaciones posibles.
        luego se podria tener 2 a la 7 -2 de ordenadores con cada subred.
    + En una red de clase C con máscara `255.255.255.192`, ¿cuántos ordenadores se pueden tener en cada subred?
    + - Como se toman prestado dos bits de la máscara quedarían 6 bits para identificar un ordenador dentro de cada subred. Con 6 bits hay 2 a la 6 combinaciones posibles. 
         luego se podría tener 2 a la 6 -2 de ordenadores con cada subred.
18. Tu empresa tiene una dirección de red de Clase B de `150.10.0.0`. Desea subdividir la red física en 3 subredes.

    + Indica una máscara que permita dividir la red de clase B (al menos) en tres subredes.
    + - 255.255.192.0       
    + ¿Cuántos hosts puede haber por subred?
    + - 2 a la 14 -2      
    + ¿Cuál es la dirección de red y la dirección de broadcast de cada una de las 3 subredes creadas?
    
<center>       
     
| Número de red | Dirección de red    | Dirección de Broadcast |
|---------------|---------------------|------------------------|
|  1            |   150.10.0.0        |  150.10.63.255         |        
|  2            |   150.10.64.0       |  150.10.127.255        |            
|  3            |   150.10.128.0      |  150.10.191.255        |            
</center>

19. Dada la dirección de clase B `120.32.0.0`, indica qué máscara de subred deberías escoger para tener 4 subredes. Rellena a continuación la siguiente tabla.

<center>

| Número de red | Dirección de subred | Primer host | Último host  |
|---------------|---------------------|-------------|--------------|
| 1             | 120.32.0.0          | 120.32.0.1  |120.32.63.254 |
| 2             | 120.32.64.0         | 120.32.64.1 |120.32.127.254|
| 3             | 120.32.128.0        | 120.32.128.1|120.32.191.254|
| 4             | 120.32.192.0        | 120.32.192.1|120.32.255.254|

</center>

20. Responde a las siguientes preguntas:

    + Si tenemos una red `150.84.32.0` con máscara de red `255.255.255.224`, indica la dirección de broadcast, la de red y la de los posibles nodos de la red.
    + - Dirección de red: 150.84.32.0        
    <br>Dirección de Broadcast:150.84.32.0
    <br>Primer Ordenador: 150.84.32.1
    <br>Ultimo Ordenador: 150.84.32.30
    + La red `192.168.0.0`, ¿de qué clase es?
    + - Clase C
    + Escribe el rango de direcciones `ip` que pertenecen a la subred definida por la dirección  `150.84.32.245` con máscara `255.255.255.240`.
    + - La Subred es 150.84.32.240
    <br>Primer Ordenador: 150.84.32.241
    <br>Ultimo Ordenador: 150.84.32.254
    + Una red de clase B en Internet tiene una máscara de subred igual a `255.255.240.0`. ¿Cuál es el máximo de nodos por subred?
    + - 2 a la 12 -2
