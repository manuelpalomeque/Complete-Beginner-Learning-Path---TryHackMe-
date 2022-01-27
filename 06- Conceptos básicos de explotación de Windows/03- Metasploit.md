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

