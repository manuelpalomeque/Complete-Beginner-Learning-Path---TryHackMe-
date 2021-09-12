## El modelo OSI: una descripción general:

¿Qué capa elegiría enviar datos a través de TCP o UDP?

    4- Transporte

¿Qué capa verifica los paquetes recibidos para asegurarse de que no se hayan dañado?

    2- Enlace de Datos

¿En qué capa se formatearían los datos en preparación para la transmisión?

    2- Enlace de Datos

¿Qué capa transmite y recibe datos?

    1- Fisica

¿Qué capa cifra, comprime o transforma los datos iniciales para darles un formato estandarizado?

    6- Presentación

¿Qué capa rastrea las comunicaciones entre el host y las computadoras receptoras?

    5- Sesión

¿Qué capa acepta solicitudes de comunicación de las aplicaciones?

    7- Aplicación

¿Qué capa maneja el direccionamiento lógico?

    3- Red

Al enviar datos a través de TCP , ¿cómo llamaría a los datos "del tamaño de un bocado"?

    Segments

[Investigación] ¿Con qué capa se comunicaría el protocolo FTP ?

    7- Aplicación

¿Qué protocolo de capa de transporte sería el más adecuado para transmitir un video en vivo?

    UDP

## Encapsulación:

¿Cómo se referiría a los datos en la capa 2 del proceso de encapsulación (con el modelo OSI)?

    Frames

¿Cómo se referiría a los datos en la capa 4 del proceso de encapsulación (con el modelo OSI), si se ha seleccionado el protocolo UDP ?

    Datagrams

¿Qué proceso realizaría una computadora en un mensaje recibido?

    De-encapsulation

¿Cuál es la única capa del modelo OSI que agrega un tráiler  durante la encapsulación?

    Data Link

¿La encapsulación proporciona una capa adicional de seguridad (Sí/No) ?

    Yes

## El modelo TCP/IP:

¿Qué modelo se introdujo primero, OSI o TCP/IP?

    TCP/IP

¿Qué capa del modelo TCP/IP cubre la funcionalidad de la capa de transporte del modelo OSI (Nombre completo) ?

    Transport

¿Qué capa del modelo TCP/IP cubre la funcionalidad de la capa de sesión del modelo OSI (Nombre completo) ?

    Application

La capa de interfaz de red del modelo TCP/IP cubre la funcionalidad de dos capas en el modelo OSI. Estas capas son Data Link y?.. (Nombre completo) ?

    Physical

¿Qué capa del modelo TCP/IP maneja la funcionalidad de la capa de red OSI?

    Internet

¿Qué tipo de protocolo es TCP?

    Connection-based

¿Qué significa SYN?

    Synchronise

¿Cuál es el segundo paso del apretón de manos de tres vías?

    SYN/ACK

¿Cuál es el nombre abreviado del segmento "Reconocimiento" en el apretón de manos de tres vías?

    ACK

## Herramientas de red: PING

¿Qué comando usaría para hacer ping al sitio web bbc.co.uk?

    cisco@labvm:~$ ping bbc.co.uk

Ping muirlandoracle.co.uk ¿Cuál es la dirección IPv4?

    cisco@labvm:~$ ping muirlandoracle.co.uk
    PING muirlandoracle.co.uk (217.160.0.152) 56(84) bytes of data.
    64 bytes from 217-160-0-152.elastic-ssl.ui-r.com (217.160.0.152): icmp_seq=1 ttl=52 time=252 ms
    64 bytes from 217-160-0-152.elastic-ssl.ui-r.com (217.160.0.152): icmp_seq=2 ttl=52 time=252 ms
    64 bytes from 217-160-0-152.elastic-ssl.ui-r.com (217.160.0.152): icmp_seq=3 ttl=52 time=254 ms
    ^C
    --- muirlandoracle.co.uk ping statistics ---
    3 packets transmitted, 3 received, 0% packet loss, time 2012ms
    rtt min/avg/max/mdev = 251.815/252.704/253.995/0.934 m
        
    217.160.0.152

¿Qué interruptor le permite cambiar el intervalo de las solicitudes de ping enviadas?

    cisco@labvm:~$ man ping

    -i interval
           Wait interval seconds between sending each packet. The default is to wait for one
           second between each packet normally, or not to wait in flood mode. Only super-user
           may set interval to values less than 0.2 seconds.

¿Qué conmutador le permitiría restringir las solicitudes a IPv4?

    cisco@labvm:~$ man ping
    
    -4
               Use IPv4 only.

¿Qué interruptor le daría una salida más detallada?

    cisco@labvm:~$ man ping

    -v
           Verbose output.
