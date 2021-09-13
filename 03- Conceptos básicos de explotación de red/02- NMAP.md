## Introducción:

¿Qué construcciones de red se utilizan para dirigir el tráfico a la aplicación correcta en un servidor?

    Ports

¿Cuántos de estos están disponibles en cualquier computadora habilitada para red?

    65535

[Investigación] ¿Cuántos de estos se consideran "bien conocidos"? (Estos son los números "estándar" mencionados en la 
tarea)

    1024

## Conmutadores Nmap

¿Cuál es el primer interruptor que aparece en el menú de ayuda para un 'Syn Scan' (más sobre esto más adelante)?

    cisco@labvm:~$ nmap -h

    SCAN TECHNIQUES:
      -sS/sT/sA/sW/sM: TCP SYN/Connect()/ACK/Window/Maimon scans
    
    -sS

¿Qué interruptor usaría para un "escaneo UDP"?

    -sU: UDP Scan

Si quisiera detectar en qué sistema operativo se está ejecutando el objetivo, ¿qué interruptor usaría?

    OS DETECTION:
        -O: Enable OS detection

Nmap proporciona un interruptor para detectar la versión de los servicios que se ejecutan en el objetivo. ¿Qué es este 
interruptor?

    SERVICE/VERSION DETECTION:
        -sV: Probe open ports to determine service/version info

La salida predeterminada proporcionada por nmap a menudo no proporciona suficiente información para un pentester. ¿Cómo
aumentarías la verbosidad?

    -v: Increase verbosity level (use -vv or more for greater effect)

El nivel de verbosidad uno es bueno, ¡pero el nivel de verbosidad dos es mejor! ¿Cómo establecería el nivel de 
verbosidad en dos?
(Nota : es muy recomendable usar siempre al menos esta opción)

    -vv

Siempre debemos guardar el resultado de nuestros escaneos; esto significa que solo necesitamos ejecutar el escaneo una 
vez (lo que reduce el tráfico de red y, por lo tanto, la posibilidad de detección), y nos brinda una referencia para 
usar al escribir informes para los clientes.

¿Qué interruptor usaría para guardar los resultados de nmap en tres formatos principales?

    -oA <basename>: Output in the three major formats at once

¿Qué interruptor usaría para guardar los resultados de nmap en un formato "normal"?

    OUTPUT:
      -oN/-oX/-oS/-oG <file>: Output scan in normal, XML, s|<rIpt kIddi3,
         and Grepable format, respectively, to the given filename.

    -oN

Un formato de salida muy útil: ¿cómo guardaría los resultados en un formato "grepable"?

    -oG

A veces, los resultados que obtenemos no son suficientes. Si no nos importa lo ruidosos que somos, podemos habilitar el 
modo "agresivo". Este es un interruptor abreviado que activa la detección de servicios, la detección del sistema 
operativo, una ruta de rastreo y un escaneo de script común.

¿Cómo activarías esta configuración?

    -A: Enable OS detection, version detection, script scanning, and traceroute

Nmap ofrece cinco niveles de plantilla de "tiempo". Estos se utilizan esencialmente para aumentar la velocidad a la que 
se ejecuta el análisis. Sin embargo, tenga cuidado: las velocidades más altas son más ruidosas y pueden incurrir en 
errores.

¿Cómo establecería la plantilla de tiempo en el nivel 5?

    -T<0-5>: Set timing template (higher is faster)

    -T5

También podemos elegir qué puerto(s) escanear.

¿Cómo le dirías a nmap que solo escanee el puerto 80?

    -p 80

¿Cómo le dirías a nmap que escanee los puertos 1000-1500?

    -p 1000-1500

Una opción muy útil que no debe ser ignorada:

¿Cómo le dirías a nmap que escanee todos los puertos?

    -p-

¿Cómo activaría un script de la biblioteca de scripts de nmap (mucho más sobre esto más adelante)?

    --script

¿Cómo activaría todos los scripts en la categoría "vuln"?

    --script=<Lua scripts>: <Lua scripts> is a comma separated list of
               directories, script-files or script-categories    
    
    --script=vuln

## Tipos de escaneo: Exploraciones de conexión TCP (-sT):

¿Qué RFC define el comportamiento apropiado para el protocolo TCP ?

    RFC 793

Si un puerto está cerrado, ¿qué indicador debe devolver el servidor para indicarlo?

    RST

## Tipos de escaneo: Escaneos SYN (-sS):

Hay otros dos nombres para un escaneo SYN, ¿cuáles son?

    Half-Open, Stealth

¿Puede Nmap usar un escaneo SYN sin permisos de Sudo (Y/N)?

    No

## Tipos de escaneo: Escaneos UDP (-sU)

Si un puerto UDP no responde a un escaneo de Nmap, ¿cómo se marcará?

    open|filtered

Cuando se cierra un puerto UDP , por convención, el objetivo debe devolver un mensaje de "puerto inalcanzable". ¿Qué protocolo usaría para hacerlo?

    ICMP

## Tipos de escaneo: NULL (-sN), FIN (-sF) y Xmas (-sX):

¿Cuál de los tres tipos de exploración mostrados utiliza el indicador URG?

    xmas

¿Por qué se utilizan generalmente los escaneos NULL, FIN y Xmas?

    Firewall Evasion

¿Qué sistema operativo común puede responder a un escaneo NULL, FIN o Xmas con un RST para cada puerto?

    Microsoft Windows

## Tipos de escaneo: Exploración de red ICMP (-sn)


¿Cómo realizaría un barrido de ping en la red 172.16.xx (máscara de red: 255.255.0.0) usando Nmap? (notación CIDR)

    cisco@labvm:~$ nmap -sn 172.16.0.0/16

## NSE Scripts

¿En qué idioma están escritos los scripts NSE?

    Lua

¿Qué categoría de secuencias de comandos sería una muy mala idea para ejecutar en un entorno de producción?

    intrusive

## NSE Scripts: Trabajando con la NSE

¿Qué argumento opcional puede ftp-anon.nsetomar el script?

    maxlist
    fuente: https://nmap.org/nsedoc/scripts/ftp-anon.html

