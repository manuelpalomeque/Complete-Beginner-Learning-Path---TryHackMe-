## Inicializando...

Podemos iniciar la consola de Metasploit en la línea de comandos sin mostrar el banner ni ninguna información de inicio.
¿Qué interruptor le agregamos a msfconsole para iniciarlo sin mostrar esta información? Esto incluirá el ' - '

    -q

¡Frio! Nos hemos conectado a la base de datos, ¿qué tipo de base de datos usa Metasploit 5? 

    postgresql

## Rock 'em to the Core [Comandos]

El menú de ayuda tiene un alias muy corto de un carácter, ¿qué es?
 
    ?

Encontrar varios módulos que tenemos a nuestra disposición dentro de Metasploit es uno de los comandos más comunes que aprovecharemos en el marco. ¿Cuál es el comando base que usamos para buscar?
 
    search

Una vez que hayamos encontrado el módulo que queremos aprovechar, ¿qué comando usamos para seleccionarlo como el módulo activo?
 
    use

¿Qué tal si queremos ver información sobre un módulo específico o solo el activo que hemos seleccionado?
 
    info

Metasploit tiene una función integrada similar a netcat donde podemos hacer una conexión rápida con un host simplemente para verificar que podemos 'hablar' con él. ¿Qué comando es este?
 
    connect

Completamente uno de los comandos utilizados puramente por diversión, ¿qué comando muestra el arte motd/ascii que vemos cuando iniciamos msfconsole (sin el indicador -q)?
 
    banner

Revisaremos estos dos próximos comandos en breve, sin embargo, son dos de los comandos más utilizados dentro de Metasploit. Primero, ¿qué comando usamos para cambiar el valor de una variable?
 
    set

Metasploit admite el uso de variables globales, algo que es increíblemente útil cuando te enfocas específicamente en un 
 solo cuadro. ¿Qué comando cambia el valor de una variable globalmente? 
 
    setg

Ahora que hemos aprendido a cambiar el valor de las variables, ¿cómo las vemos? Técnicamente, hay varias respuestas a 
 esta pregunta, sin embargo, estoy buscando un comando específico de tres letras que se use para ver el valor de 
 variables individuales.
 
    get

¿Qué hay de cambiar el valor de una variable a nulo/sin valor?
 
    unset

Al realizar una prueba de penetración, es bastante común grabar su pantalla para una revisión adicional o para 
 proporcionar evidencia de las acciones realizadas. Esto a menudo se combina con la recopilación de la salida de la 
 consola en un archivo, ya que puede ser increíblemente útil para buscar diferentes piezas de información en la 
 pantalla. ¿Qué comando podemos usar para configurar la salida de nuestra consola para guardarla en un archivo?
 
    spool

Dejar una consola de Metasploit en ejecución no siempre es conveniente y puede ser útil tener todos nuestros valores 
 establecidos previamente cargados al iniciar Metasploit. ¿Qué comando podemos usar para almacenar la 
 configuración/almacenes de datos activos de Metasploit en un archivo de configuración? Esto se guardará en su 
 directorio msf4 (o msf5) y se puede deshacer fácilmente simplemente eliminando el archivo de configuración creado.
 
    save

## Módulos para cada ocasión
 
Fácilmente el módulo más común utilizado, ¿qué módulo contiene todo el código de explotación que usaremos?
 
    exploit

Usado junto con exploits, ¿qué módulo contiene los diversos bits de shellcode que enviamos para que se ejecuten después de la explotación?
 
    payload

¿Qué módulo se usa más comúnmente en las máquinas de escaneo y verificación son explotables? Esto no es lo mismo que la explotación real, por supuesto.
 
    auxiliary

Una de las actividades más comunes después de la explotación es el saqueo y el pivoteo. ¿Qué módulo proporciona estas capacidades?
 
    post

Comúnmente utilizado en la ofuscación de la carga útil, ¿qué módulo nos permite modificar la "apariencia" de nuestro exploit para que podamos evitar la detección de firmas?
 
    encoder

Por último, pero no menos importante, ¿qué módulo se usa con desbordamiento de búfer y ataques ROP?
 
    nop

No todos los módulos se cargan de forma predeterminada, ¿qué comando podemos usar para cargar diferentes módulos? 
 
    load

## Move The Shell

¿Qué servicio identifica nmap ejecutándose en el puerto 135?

    msrpc

Ahora que hemos escaneado el sistema de nuestra víctima, intentemos conectarnos con una carga útil de Metasploit. 
Primero, tendremos que buscar la carga útil de destino. En Metasploit 5 (la versión más reciente en el momento de 
escribir este artículo), simplemente puede escribir useseguido de una cadena única que se encuentra solo dentro del 
exploit de destino. Por ejemplo, pruebe esto ahora con el siguiente comando use icecast. ¿Cuál es la ruta completa de
nuestro exploit que ahora aparece en el indicador de msfconsole? *Esto incluirá la sección de explotación al principio

    exploit/windows/http/icecast_header

¿Cuál es el nombre de la columna en el extremo izquierdo de la consola que aparece junto a 'Nombre'?

    #

## Estamos dentro, ¿ahora qué?

Lo primero es lo primero, nuestro shell/proceso inicial normalmente no es muy estable. Sigamos adelante e intentemos pasar a un proceso diferente. Primero, enumeremos los procesos usando el comando ps. ¿Cuál es el nombre del servicio de cola?
 
    spoolsv.exe

¡Sigamos adelante y pasemos al proceso de spool o al menos intentemos hacerlo! ¿Qué comando usamos para transferirnos al proceso? Esto no funcionará en este momento ya que no tenemos suficientes privilegios, ¡pero aún podemos intentarlo!
 
    migrate

Bueno, esa migración no funcionó, busquemos más información sobre el sistema para que podamos intentar elevarlo. ¿Qué comando podemos ejecutar para obtener más información sobre el usuario actual que ejecuta el proceso en el que nos encontramos?
 
    getuid

¿Qué tal encontrar más información sobre el sistema en sí?
 
    sysinfo

Esto puede requerir un poco de búsqueda en Google, ¿qué ejecutamos para cargar mimikatz (más específicamente, la nueva versión de mimikatz) para que podamos usarlo? 
 
    load kiwi

Avancemos y averigüemos los privilegios de nuestro usuario actual, ¿qué comando ejecutamos?
 
    getprivs

¿Qué comando ejecutamos para transferir archivos a nuestra computadora víctima?
 
    c

¿Qué tal si queremos ejecutar un módulo de Metasploit?
 
    run

Una pregunta simple pero aún bastante necesaria, ¿qué comando ejecutamos para averiguar la información de red y las interfaces de nuestra víctima?

    ipconfig

Una pregunta adicional rápida, ¿qué comando podemos ejecutar en nuestra sesión de meterpreter para generar un shell de sistema normal? 

    shell

