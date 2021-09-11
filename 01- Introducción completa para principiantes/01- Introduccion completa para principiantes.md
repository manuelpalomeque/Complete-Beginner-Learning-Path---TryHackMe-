## Tutorial:

¿Cuál es el texto del indicador que se muestra en el sitio web de la máquina que inició en esta tarea?

    flag{connection_verified}

## Seguridad Ofensiva:

¿Cómo se llama el puesto de carrera que se emplea legalmente para encontrar vulnerabilidades en las aplicaciones?

    penetration tester

## Seguridad defensiva:

¿Cuál es el nombre del rol cuyo trabajo es identificar los ataques contra una organización?

    security analyst

## Introducción a la investigación:

En esta sala se fortalece la habilidad de investigacion de diferentes temas.


1) Ejemplos de preguntas de investigación:

En el programa Burp Suite que se incluye con Kali Linux, ¿qué modo usaría para enviar manualmente una solicitud (a menudo repitiendo una solicitud capturada varias veces)?

    Repeater

¿En qué formato hash se almacenan las contraseñas modernas de inicio de sesión de Windows?

    NTLM

¿Cómo se llaman las tareas automatizadas en Linux?

    Cron Jobs

¿Qué base numérica podrías usar como abreviatura de base 2 (binario)?

    Base 16

Si un hash de contraseña comienza con $ 6 $, ¿qué formato tiene (variante de Unix)?

    sha512crypt

2) Búsqueda de vulnerabilidades:

¿Cuál es el CVE para la vulnerabilidad 2020 Cross-Site Scripting (XSS) que se encuentra en WPForms?

    fuente: https://www.exploit-db.com/exploits/48245

    CVE-2020-10385

    WordPress Plugin WPForms 1.5.8.2 - Persistent Cross-Site Scripting

    EDB-ID:48245
    CVE:2020-10385

    Author:JINSON VARGHESE BEHANAN
    Type:WEBAPPS
    
    Platform: PHP
    Date:2020-03-2

Se encontró una vulnerabilidad de escalada de privilegios locales en la versión Debian  de Apache Tomcat, en 2016. ¿Cuál es el CVE para esta vulnerabilidad?

    fuente: https://www.exploit-db.com/exploits/40450
    
    CVE-2016-1240
    
    Apache Tomcat 8/7/6 (Debian-Based Distros) - Local Privilege Escalation
    
    EDB-ID:40450
    CVE:2016-1240
    
    Author:DAWID GOLUNSKI
    Type:LOCAL
    
    Platform:LINUX
    Date:2016-10-03

¿Cuál es el primer CVE encontrado en el reproductor multimedia VLC?

    fuente:  https://www.exploit-db.com/exploits/3069
    
    CVE-2007-0017
    
    VideoLAN VLC Media Player 0.8.6 (PPC) - 'udp://' Format String (PoC)
    
    EDB-ID:3069
    CVE:2007-0017
    
    Author:MOAB
    Type:DOS
    
    Platform:OSX
    Date:2007-01-02

Si quisiera explotar un desbordamiento de búfer de 2020 en el programa Sudo, ¿qué CVE usaría?

    fuente: https://www.exploit-db.com/exploits/48052
    
    CVE-2019-18634
    
    Sudo 1.8.25p - 'pwfeedback' Buffer Overflow
    
    EDB-ID: 48052
    CVE: 2019-18634
    
    Author:DYLAN KATZ
    Type:LOCAL
    
    Platform:LINUX
    Date:2020-02-06

3) Páginas de manuales

SCP es una herramienta utilizada para copiar archivos de una computadora a otra.
¿Qué interruptor usaría para copiar un directorio completo?

    cisco@labvm:~$ man scp

    -r      Recursively copy entire directories.  Note that scp follows sym‐
             bolic links encountered in the tree traversal.

fdisk es un comando que se utiliza para ver y modificar el esquema de partición utilizado en su disco duro.
¿Qué interruptor usaría para enumerar las particiones actuales?

    cisco@labvm:~$ man fdisk

    -l, --list
          List the partition tables for the specified devices and then exit.  If no devices are given, those mentioned
          in /proc/partitions (if that file exists) are used.


nano es un editor de texto fácil de usar para Linux . Podría decirse que hay mejores editores (Vim, siendo la elección obvia); sin embargo, nano es excelente para empezar.
¿Qué interruptor usarías para hacer una copia de seguridad al abrir un archivo con nano?

    cisco@labvm:~$ man nano

    -B, --backup
            When saving a file, back up the previous version of it, using the current filename  suffixed  with  a  tilde
            (~).

Netcat es una herramienta básica utilizada para enviar y recibir manualmente solicitudes de red. 
¿Qué comando  usaría para iniciar netcat en modo de escucha, usando el puerto 12345?

    cisco@labvm:~$ man nc

    -l      Listen for an incoming connection rather than initiating a connection to a remote host.  The destination and
             port to listen on can be specified either as non-optional arguments, or with options -s and -p respectively.
             Cannot be used together with -x or -z.  Additionally, any timeouts specified with the -w option are ignored.

    -p source_port
             Specify the source port nc should use, subject to privilege restrictions and availability.

    cisco@labvm:~$ nc -l -p 12345




