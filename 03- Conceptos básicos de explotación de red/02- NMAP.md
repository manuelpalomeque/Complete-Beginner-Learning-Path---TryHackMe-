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

## NSE Scripts: Búsqueda de Scripts

Busque secuencias de comandos "smb" en el /usr/share/nmap/scripts/directorio utilizando cualquiera de los métodos 
demostrados. ¿Cuál es el nombre de archivo del script que determina el sistema operativo subyacente del servidor SMB?

    cisco@labvm:/usr/share/nmap/scripts$ ls -l /usr/share/nmap/scripts/*smb*
    -rw-r--r-- 1 root root  3355 Mar 23  2020 /usr/share/nmap/scripts/smb2-capabilities.nse
    -rw-r--r-- 1 root root  3075 Mar 23  2020 /usr/share/nmap/scripts/smb2-security-mode.nse
    -rw-r--r-- 1 root root  1447 Mar 23  2020 /usr/share/nmap/scripts/smb2-time.nse
    -rw-r--r-- 1 root root  5238 Mar 23  2020 /usr/share/nmap/scripts/smb2-vuln-uptime.nse
    -rw-r--r-- 1 root root 45138 Mar 23  2020 /usr/share/nmap/scripts/smb-brute.nse
    -rw-r--r-- 1 root root  5289 Mar 23  2020 /usr/share/nmap/scripts/smb-double-pulsar-backdoor.nse
    -rw-r--r-- 1 root root  4840 Mar 23  2020 /usr/share/nmap/scripts/smb-enum-domains.nse
    -rw-r--r-- 1 root root  5971 Mar 23  2020 /usr/share/nmap/scripts/smb-enum-groups.nse
    -rw-r--r-- 1 root root  8043 Mar 23  2020 /usr/share/nmap/scripts/smb-enum-processes.nse
    -rw-r--r-- 1 root root 27274 Mar 23  2020 /usr/share/nmap/scripts/smb-enum-services.nse
    -rw-r--r-- 1 root root 12097 Mar 23  2020 /usr/share/nmap/scripts/smb-enum-sessions.nse
    -rw-r--r-- 1 root root  6923 Mar 23  2020 /usr/share/nmap/scripts/smb-enum-shares.nse
    -rw-r--r-- 1 root root 12527 Mar 23  2020 /usr/share/nmap/scripts/smb-enum-users.nse
    -rw-r--r-- 1 root root  1706 Mar 23  2020 /usr/share/nmap/scripts/smb-flood.nse
    -rw-r--r-- 1 root root  7393 Mar 23  2020 /usr/share/nmap/scripts/smb-ls.nse
    -rw-r--r-- 1 root root  8758 Mar 23  2020 /usr/share/nmap/scripts/smb-mbenum.nse
    -rw-r--r-- 1 root root  8220 Mar 23  2020 /usr/share/nmap/scripts/smb-os-discovery.nse
    -rw-r--r-- 1 root root  4982 Mar 23  2020 /usr/share/nmap/scripts/smb-print-text.nse
    -rw-r--r-- 1 root root  1898 Mar 23  2020 /usr/share/nmap/scripts/smb-protocols.nse
    -rw-r--r-- 1 root root 63596 Mar 23  2020 /usr/share/nmap/scripts/smb-psexec.nse
    -rw-r--r-- 1 root root  5190 Mar 23  2020 /usr/share/nmap/scripts/smb-security-mode.nse
    -rw-r--r-- 1 root root  2424 Mar 23  2020 /usr/share/nmap/scripts/smb-server-stats.nse
    -rw-r--r-- 1 root root 14159 Mar 23  2020 /usr/share/nmap/scripts/smb-system-info.nse
    -rw-r--r-- 1 root root  7524 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-conficker.nse
    -rw-r--r-- 1 root root  6402 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-cve2009-3103.nse
    -rw-r--r-- 1 root root 23154 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-cve-2017-7494.nse
    -rw-r--r-- 1 root root  6545 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-ms06-025.nse
    -rw-r--r-- 1 root root  5386 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-ms07-029.nse
    -rw-r--r-- 1 root root  5688 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-ms08-067.nse
    -rw-r--r-- 1 root root  5647 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-ms10-054.nse
    -rw-r--r-- 1 root root  7214 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-ms10-061.nse
    -rw-r--r-- 1 root root  7344 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-ms17-010.nse
    -rw-r--r-- 1 root root  4400 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-regsvc-dos.nse
    -rw-r--r-- 1 root root  6586 Mar 23  2020 /usr/share/nmap/scripts/smb-vuln-webexec.nse
    -rw-r--r-- 1 root root  5105 Mar 23  2020 /usr/share/nmap/scripts/smb-webexec-exploit.nse
      
    /usr/share/nmap/scripts/smb-os-discovery.nse 
    smb-os-discovery.nse

Lea este script. ¿De qué depende?

    smb-brute

## Evasión de Firewalls
¿Qué protocolo simple (y en el que se confía con frecuencia) se bloquea a menudo y requiere el uso del -Pnconmutador?

    ICMP

[Investigación] ¿Qué conmutador Nmap le permite agregar una longitud arbitraria de datos aleatorios al final de los paquetes?

    --data-length

    fuente: https://nmap.org/book/man-bypass-firewalls-ids.html

## Challenge:

¿El objetivo ( 10.10.167.149) responde a las solicitudes ICMP (ping) (S/N)?

    root@ip-10-10-78-68:~# ping -c 4  10.10.167.149
    PING 10.10.167.149 (10.10.167.149) 56(84) bytes of data.
    
    --- 10.10.167.149 ping statistics ---
    4 packets transmitted, 0 received, 100% packet loss, time 3056ms

    No

Realice un escaneo Xmas en los primeros 999 puertos del objetivo: ¿cuántos puertos se muestran abiertos o filtrados?

    root@ip-10-10-78-68:~# nmap -sX -p 1-999  10.10.167.149

    Starting Nmap 7.60 ( https://nmap.org ) at 2022-02-13 16:34 GMT
    Nmap scan report for ip-10-10-167-149.eu-west-1.compute.internal (10.10.167.149)
    Host is up (0.00015s latency).
    All 999 scanned ports on ip-10-10-167-149.eu-west-1.compute.internal (10.10.167.149) are open|filtered
    MAC Address: 02:5A:73:AF:01:E5 (Unknown)
    
    Nmap done: 1 IP address (1 host up) scanned in 21.42 seconds  
    
    999

Hay una razón dada para esto, ¿cuál es?
Nota: La respuesta estará en los resultados de su escaneo. Piense detenidamente qué interruptores usar y lea la 
sugerencia antes de pedir ayuda. ---> USAR EL COMANDO  -VV

    root@ip-10-10-78-68:~# nmap -sX -p 1-999 -vv 10.10.167.149
    
    Starting Nmap 7.60 ( https://nmap.org ) at 2022-02-13 16:26 GMT
    Initiating ARP Ping Scan at 16:26
    Scanning 10.10.167.149 [1 port]
    Completed ARP Ping Scan at 16:26, 0.22s elapsed (1 total hosts)
    Initiating Parallel DNS resolution of 1 host. at 16:26
    Completed Parallel DNS resolution of 1 host. at 16:26, 0.00s elapsed
    Initiating XMAS Scan at 16:26
    Scanning ip-10-10-167-149.eu-west-1.compute.internal (10.10.167.149) [999 ports]
    Completed XMAS Scan at 16:26, 21.08s elapsed (999 total ports)
    Nmap scan report for ip-10-10-167-149.eu-west-1.compute.internal (10.10.167.149)
    Host is up, received arp-response (0.00013s latency).
    All 999 scanned ports on ip-10-10-167-149.eu-west-1.compute.internal (10.10.167.149) are open|filtered because of 999 no-responses
    MAC Address: 02:5A:73:AF:01:E5 (Unknown)
    
    Read data files from: /usr/bin/../share/nmap
    Nmap done: 1 IP address (1 host up) scanned in 21.43 seconds
               Raw packets sent: 1999 (79.948KB) | Rcvd: 1 (28B)
      
    
    No Response

Realice un escaneo TCP SYN en los primeros 5000 puertos del objetivo: ¿cuántos puertos se muestran abiertos?

    root@ip-10-10-78-68:~# nmap -sS -p 0-5000 -vv 10.10.167.149
    
    Starting Nmap 7.60 ( https://nmap.org ) at 2022-02-13 16:15 GMT
    Initiating ARP Ping Scan at 16:15
    Scanning 10.10.167.149 [1 port]
    Completed ARP Ping Scan at 16:15, 0.22s elapsed (1 total hosts)
    Initiating Parallel DNS resolution of 1 host. at 16:15
    Completed Parallel DNS resolution of 1 host. at 16:15, 0.00s elapsed
    Initiating SYN Stealth Scan at 16:15
    Scanning ip-10-10-167-149.eu-west-1.compute.internal (10.10.167.149) [5001 ports]
    Discovered open port 3389/tcp on 10.10.167.149
    Discovered open port 53/tcp on 10.10.167.149
    Discovered open port 21/tcp on 10.10.167.149
    Discovered open port 135/tcp on 10.10.167.149
    Discovered open port 80/tcp on 10.10.167.149
    Increasing send delay for 10.10.167.149 from 0 to 5 due to 11 out of 28 dropped probes since last increase.
    SYN Stealth Scan Timing: About 33.21% done; ETC: 16:17 (0:01:02 remaining)
    Increasing send delay for 10.10.167.149 from 5 to 10 due to 11 out of 29 dropped probes since last increase.
    Increasing send delay for 10.10.167.149 from 10 to 20 due to 11 out of 34 dropped probes since last increase.
    SYN Stealth Scan Timing: About 60.52% done; ETC: 16:18 (0:01:01 remaining)
    Increasing send delay for 10.10.167.149 from 20 to 40 due to 11 out of 34 dropped probes since last increase.
    Increasing send delay for 10.10.167.149 from 40 to 80 due to 11 out of 32 dropped probes since last increase.
    SYN Stealth Scan Timing: About 68.24% done; ETC: 16:19 (0:01:13 remaining)
    SYN Stealth Scan Timing: About 74.07% done; ETC: 16:21 (0:01:21 remaining)
    SYN Stealth Scan Timing: About 80.34% done; ETC: 16:22 (0:01:17 remaining)
    SYN Stealth Scan Timing: About 86.40% done; ETC: 16:23 (0:01:02 remaining)
    SYN Stealth Scan Timing: About 91.28% done; ETC: 16:24 (0:00:43 remaining)
    Completed SYN Stealth Scan at 16:25, 565.93s elapsed (5001 total ports)
    Nmap scan report for ip-10-10-167-149.eu-west-1.compute.internal (10.10.167.149)
    Host is up, received arp-response (0.0017s latency).
    Scanned at 2022-02-13 16:15:57 GMT for 566s
    Not shown: 4996 filtered ports
    Reason: 4996 no-responses
    PORT     STATE SERVICE       REASON
    21/tcp   open  ftp           syn-ack ttl 128
    53/tcp   open  domain        syn-ack ttl 128
    80/tcp   open  http          syn-ack ttl 128
    135/tcp  open  msrpc         syn-ack ttl 128
    3389/tcp open  ms-wbt-server syn-ack ttl 128
    MAC Address: 02:5A:73:AF:01:E5 (Unknown)
    
    Read data files from: /usr/bin/../share/nmap
    Nmap done: 1 IP address (1 host up) scanned in 566.29 seconds
               Raw packets sent: 15436 (679.168KB) | Rcvd: 448 (19.696KB)    
    
    5

Abra Wireshark (consulte Wireshark Room de Cryillic para obtener instrucciones) y realice un escaneo de conexión TCP contra el puerto 80 en el objetivo, monitoreando los resultados. Asegúrate de entender lo que está pasando.

    No se necesita respuesta

Despliegue el ftp-anonscript contra la caja. ¿Puede Nmap iniciar sesión con éxito en el servidor FTP en el puerto 21? (S/N)

    Y
