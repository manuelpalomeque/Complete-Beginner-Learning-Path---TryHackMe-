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

    -sS

¿Qué interruptor usaría para un "escaneo UDP"?

    -sU

Si quisiera detectar en qué sistema operativo se está ejecutando el objetivo, ¿qué interruptor usaría?

    -O

Nmap proporciona un interruptor para detectar la versión de los servicios que se ejecutan en el objetivo. ¿Qué es este 
interruptor?

    -sV

La salida predeterminada proporcionada por nmap a menudo no proporciona suficiente información para un pentester. ¿Cómo
aumentarías la verbosidad?

    -v

El nivel de verbosidad uno es bueno, ¡pero el nivel de verbosidad dos es mejor! ¿Cómo establecería el nivel de 
verbosidad en dos?
(Nota : es muy recomendable usar siempre al menos esta opción)

    -vv

Siempre debemos guardar el resultado de nuestros escaneos; esto significa que solo necesitamos ejecutar el escaneo una 
vez (lo que reduce el tráfico de red y, por lo tanto, la posibilidad de detección), y nos brinda una referencia para 
usar al escribir informes para los clientes.

¿Qué interruptor usaría para guardar los resultados de nmap en tres formatos principales?

    -oA

¿Qué interruptor usaría para guardar los resultados de nmap en un formato "normal"?

    -oN

Un formato de salida muy útil: ¿cómo guardaría los resultados en un formato "grepable"?

    -oG

A veces, los resultados que obtenemos no son suficientes. Si no nos importa lo ruidosos que somos, podemos habilitar el 
modo "agresivo". Este es un interruptor abreviado que activa la detección de servicios, la detección del sistema 
operativo, una ruta de rastreo y un escaneo de script común.

¿Cómo activarías esta configuración?

    -A

Nmap ofrece cinco niveles de plantilla de "tiempo". Estos se utilizan esencialmente para aumentar la velocidad a la que 
se ejecuta el análisis. Sin embargo, tenga cuidado: las velocidades más altas son más ruidosas y pueden incurrir en 
errores.

¿Cómo establecería la plantilla de tiempo en el nivel 5?

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

    --script=vuln

