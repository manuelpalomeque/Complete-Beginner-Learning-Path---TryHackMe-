## Introducción

¿Quién es el empleado del mes?

    Bill Harper

## Acceso inicial

Escanee la máquina con nmap. ¿En qué otro puerto se ejecuta un servidor web?
 
    8080

Eche un vistazo al otro servidor web. ¿Qué servidor de archivos se está ejecutando?
 
    Rejetto HttpFileServer

¿Cuál es el número CVE para explotar este servidor de archivos?
 
    2014-6287

Utilice Metasploit para obtener un shell inicial. ¿Qué es la bandera de usuario?

    b04763b6fcf51fcd7c13abc7db4fd365

## Escalada de privilegios

Preste mucha atención a la opción CanRestart que está establecida en true. ¿Cuál es el nombre del servicio que aparece
como una vulnerabilidad de ruta de servicio no citada ?

    AdvancedSystemCareService9

¿Qué es la bandera raíz?

    9af5f314f57607c00fd09803a587db80

## Acceso y escalada sin Metasploit

¿Qué comando powershell -c podríamos ejecutar para averiguar manualmente el nombre del servicio?

    powershell -c "GetService"
