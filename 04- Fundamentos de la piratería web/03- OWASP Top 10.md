## [Severity 1] Command Injection Practical
navigate to http://10.10.145.63/evilshell.php.

¿Qué archivo de texto extraño se encuentra en el directorio raíz del sitio web?
 
    EvilShell
    ls
    css drpepper.txt evilshell.php index.php js 
    
    drpeper.txt
 
¿Cuántos usuarios no root / no de servicio / no demonio (non-root/non-service/non-daemon) hay?
 
    EvilShell
    cat /etc/passwd
    root:x:0:0:root:/root:/bin/bash 
    daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nologin 
    bin:x:2:2:bin:/bin:/usr/sbin/nologin 
    sys:x:3:3:sys:/dev:/usr/sbin/nologin 
    sync:x:4:65534:sync:/bin:/bin/sync 
    games:x:5:60:games:/usr/games:/usr/sbin/nologin 
    man:x:6:12:man:/var/cache/man:/usr/sbin/nologin 
    lp:x:7:7:lp:/var/spool/lpd:/usr/sbin/nologin 
    mail:x:8:8:mail:/var/mail:/usr/sbin/nologin 
    news:x:9:9:news:/var/spool/news:/usr/sbin/nologin 
    uucp:x:10:10:uucp:/var/spool/uucp:/usr/sbin/nologin 
    proxy:x:13:13:proxy:/bin:/usr/sbin/nologin 
    www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin 
    backup:x:34:34:backup:/var/backups:/usr/sbin/nologin 
    list:x:38:38:Mailing List Manager:/var/list:/usr/sbin/nologin 
    irc:x:39:39:ircd:/var/run/ircd:/usr/sbin/nologin 
    gnats:x:41:41:Gnats Bug-Reporting System (admin):/var/lib/gnats:/usr/sbin/nologin 
    nobody:x:65534:65534:nobody:/nonexistent:/usr/sbin/nologin 
    systemd-network:x:100:102:systemd Network Management,,,:/run/systemd/netif:/usr/sbin/nologin systemd-resolve:x:101:103:
    systemd Resolver,,,:/run/systemd/resolve:/usr/sbin/nologin 
    syslog:x:102:106::/home/syslog:/usr/sbin/nologin 
    messagebus:x:103:107::/nonexistent:/usr/sbin/nologin 
    _apt:x:104:65534::/nonexistent:/usr/sbin/nologin 
    lxd:x:105:65534::/var/lib/lxd/:/bin/false 
    uuidd:x:106:110::/run/uuidd:/usr/sbin/nologin 
    dnsmasq:x:107:65534:dnsmasq,,,:/var/lib/misc:/usr/sbin/nologin 
    landscape:x:108:112::/var/lib/landscape:/usr/sbin/nologin 
    pollinate:x:109:1::/var/cache/pollinate:/bin/false 
    sshd:x:110:65534::/run/sshd:/usr/sbin/nologin 

    0

¿Con qué usuario se ejecuta esta aplicación?
  
    EvilShell  
    whoami
    www-data 

    www-data 

¿Cómo está configurado el shell del usuario?
 
    EvilShell
    cat /etc/passwd

    www-data:x:33:33:www-data:/var/www:/usr/sbin/nologin 

    /usr/sbin/nologin 

¿Qué versión de Ubuntu se está ejecutando?
 
    EvilShell
    lsb_release -a
    Distributor ID: Ubuntu 
    Description: Ubuntu 18.04.4 LTS 
    Release: 18.04 
    Codename: bionic  
    
    18.04.4
 
Imprime el MOTD. ¿Qué bebida favorita se muestra?
 
    EvilShell
    cat /etc/update-motd.d/00-header
    #!/bin/sh # # 00-header - create the header of the MOTD # Copyright (C) 2009-2010 Canonical Ltd. # 
    # Authors: Dustin Kirkland # 
    # This program is free software; you can redistribute it and/or modify # it under the terms of the GNU General 
    Public License as published by # the Free Software Foundation; either version 2 of the License, or 
    # (at your option) any later version. # # This program is distributed in the hope that it will be useful, 
    # but WITHOUT ANY WARRANTY; without even the implied warranty of 
    # MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the # GNU General Public License for more details. # 
    # You should have received a copy of the GNU General Public License along # with this program; if not, write to the 
    Free Software Foundation, Inc., # 51 Franklin Street, Fifth Floor, Boston, MA 02110-1301 USA. 
    [ -r /etc/lsb-release ] && . /etc/lsb-release if [ -z "$DISTRIB_DESCRIPTION" ] && [ -x /usr/bin/lsb_release ]; then 
    # Fall back to using the very slow lsb_release utility DISTRIB_DESCRIPTION=$(lsb_release -s -d) fi printf 
    "Welcome to %s (%s %s %s)\n" "$DISTRIB_DESCRIPTION" "$(uname -o)" "$(uname -r)" "$(uname -m)" 
    DR PEPPER MAKES THE WORLD TASTE BETTER! 
    
    DR PEPPER

## [Severity 2] Broken Authentication Practical

¿Cuál es la bandera que encontraste en la cuenta de Darren?
 
    fe86079416a21a3c99937fea8874b667
 
Ahora intente hacer el mismo truco y vea si puede iniciar sesión como arthur. 
¿Cuál es la bandera que encontraste en el relato de Arthur?

    s9ac0f7db4fda460ac3edeb75d75e16e

## [Severidad 3] Sensitive Data Exposure (Challenge)

¿Cuál es el nombre del directorio mencionado?
 
    /assets

Navegue hasta el directorio que encontró en la pregunta uno. ¿Qué archivo es probable que contenga datos sensibles?
 
    webapp.db
 
Utilice el material de apoyo para acceder a los datos confidenciales. ¿Cuál es el hash de la contraseña del usuario administrador?
 
    6eea9b7ef19179a06954edd0f6c05ceb 

Rompe el hachís.
¿Cuál es la contraseña de texto sin formato del administrador?
 
    qwertyuiop
 
Inicie sesión como administrador. ¿Qué es la bandera?

    THM{Yzc2YjdkMjE5N2VjMzNhOTE3NjdiMjdl}

## [Severity 4 XML External Entity - eXtensible Markup Language

Forma completa de XML
 
    eXtensible Markup Language

¿Es obligatorio tener XML prólogo en los documentos XML?
 
    no

¿Podemos validar documentos XML con un esquema?
 
    yes
 
¿Cómo podemos especificar la versión XML y la codificación en un documento XML?

    XML prolog

## [Severity 4] XML External Entity – DTD

¿Cómo se define un nuevo ELEMENTO?
 
    !ELEMENT

¿Cómo se define un elemento ROOT?
 
    !DOCTYPE
 
¿Cómo se define una nueva ENTIDAD?

    !ENTITY

## [Severity 4] XML External Entity – Exploiting

¿Cuál es el nombre del usuario en /etc/passwd?
 
    falcon

¿Dónde se encuentra la clave SSH de falcon?
 
    /home/falcon/.ssh/id_rsa

¿Cuáles son los primeros 18 caracteres de la clave privada de Falcon?

    MIIEogIBAAKCAQEA7b

## [Severity 5] Broken Access Control (IDOR Challenge)

Mira las notas de otros usuarios. ¿Qué es la bandera?

    flag{fivefourthree}

## [Severity 6] Security Misconfiguration 

¡Hackea la aplicación web y encuentra la bandera!

    THM{4b9513968fd564a87b28aa1f9d672e17}

## [Severity 7] Cross-site Scripting

Vaya a  http: // MACHINE_IP /  en su navegador y haga clic en la pestaña "Reflected XSS" en la barra de navegación; cree una carga útil XSS reflejada que generará una ventana emergente que diga "Hola".
 
    ThereIsMoreToXSSThanYouThink

En la misma página reflectante, cree una carga útil XSS reflejada que generará una ventana emergente con la dirección IP de su máquina.
 
    ReflectiveXss4TheWin

Ahora navegue a  http: // MACHINE_IP /  en su navegador y  haga clic en la pestaña "Stored XSS" en la barra de navegación; hacer una cuenta. 
Luego agregue un comentario y vea si puede insertar algo de su propio HTML.
 
    HTML_T4gs

En la misma página, cree que aparezca un cuadro emergente de alerta en la página con las cookies de su documento.
 
    W3LL_D0N3_LVL2

Cambie "XSS Playground" a "Soy un hacker" agregando un comentario y usando Javascript.
 
    websites_can_be_easily_defaced_with_xss

## [Severity 8] Insecure Deserialization

¿Quién desarrolló la aplicación Tomcat?
 
    the apache software foundation

¿Qué tipo de ataque que bloquea los servicios se puede realizar con deserialización insegura?
 
    denial of service

## [Severity 8] Insecure Deserialization – Objects

Seleccione el término correcto de la siguiente declaración:

si un perro estuviera durmiendo, sería esto:
A) Un estado / A State
B) Un comportamiento  / A Behaviour 

    A Behaviour  

## [Severity 8] Insecure Deserialization – Deserialization 

¿Cuál es el nombre del formato base-2 con el que se envían los datos a través de una red? 

    binary

## [Severity 8] Insecure Deserialization – Cookies

Si una cookie tuviera la ruta  webapp.com/login  , ¿cuál sería la URL que debe visitar el usuario?
 
    webapp.com/login

¿Cuál es el acrónimo de la tecnología web sobre la que   funcionan las cookies seguras ?

    HTTPS

## [Severity 8] Insecure Deserialization - Cookies Practical

1ra bandera (valor de la cookie)
 
    THM{good_old_base64_huh}

2da bandera (panel de administración)

    THM{heres_the_admin_flag}

## [Severity 8] Insecure Deserialization - Code Execution

flag.txt

    4a69a7ff9fd68

## [Severity 9] Components with Known Vulnerabilities - Lab

Cuántos caracteres hay en / etc / passwd (use wc -c / etc / passwd para obtener la respuesta)

    1611

## [Severity 10] Insufficient Logging and Monitoring

¿Qué dirección IP está usando el atacante?
 
    49.99.13.16

¿Qué tipo de ataque se está llevando a cabo?
 
    brute force


