## Reconocimiento

Escanea la máquina. (Si no está seguro de cómo abordar esto, le recomiendo que visite la sala de Nmap )
¿Cuántos puertos están abiertos con un número de puerto inferior a 1000?

    Command: nmap -sV -vv --script vuln TARGET_IP
    Solo 3 puertos son de los inferiores a  1000 el resto es superior


¿A qué es vulnerable esta máquina? (Respuesta en forma de: ms ?? - ???, ex: ms08-067)
 
    ms17-010

