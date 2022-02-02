## Implementar la máquina virtual Debian vulnerable

Ejecute el comando "id". Cual es el resultado?

    uid=1000(user) gid=1000(user) groups=1000(user),24(cdrom),25(floppy),29(audio),30(dip),44(video),46(plugdev)

## Permisos de archivo débiles - Legible /etc/shadow

¿Cuál es el hash de la contraseña del usuario root?
 
    $6$Tb/euwmK$OXA.dwMeOAcopwBl68boTG5zi65wIHsc84OWAIye5VITLLtVlaXvRDJXET..it8r.jbrlpfZeMdwD3B0fGxJI0

¿Qué algoritmo hash se usó para producir el hash de la contraseña del usuario raíz?
 
    sha512crypt

¿Cuál es la contraseña del usuario root?

    password123

## Permisos de archivo débiles - Escribible /etc/passwd

Ejecute el comando "id" como usuario newroot. Cual es el resultado?

    uid=0(root) gid=0(root) groups=0(root)

## Sudo - Secuencias de escape de Shell

¿Cuántos programas puede ejecutar el "usuario" a través de sudo? 
 
    11

Un programa de la lista no tiene una secuencia de escape de shell en GTFOBins. ¿Cuál es?

    Apache2

##  Trabajos cron - Variable de entorno PATH

¿Cuál es el valor de la variable PATH en /etc/crontab?

    /home/user:/usr/local/sbin:/usr/local/bin:/sbin:/bin:/usr/sbin:/usr/bin

## Contraseñas y claves - Archivos de historial

¿Cuál es el comando mysql completo que ejecutó el usuario?

    mysql -h somehost.local -uroot -ppassword123

## Contraseñas y claves: archivos de configuración

    /etc/openvpn/auth.txt





