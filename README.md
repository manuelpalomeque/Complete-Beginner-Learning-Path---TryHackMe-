#  Complete-Beginner-Learning-Path   👨‍💻 📚🥈

En este repositorio se encuentran practicos y challenges de diferentes tematicas realizadas en el curso.

## A) Temario:

    01- Introducción completa para principiantes
    02- Fundamentos de Linux
    03- Conceptos básicos de explotación de red
    04- Fundamentos de la piratería web
    05- Criptografía
    06- Conceptos básicos de explotación de Windows
    07- Shells y escalada de privilegios
    08- CTF: Explotación informática básica


## B) Descripción:

### ***01- Introducción completa para principiantes:*** 
Comenzando en CyberSec. Introducción a la investigación, Búsqueda de vulnerabilidades (ExploitDB, NVD, Inglete CVE), 
Páginas de manuales.

### **_02- Fundamentos de Linux:_** 
Desarrollado en el curso de pre seguridad.

 👉 <a href="https://github.com/manuelpalomeque/Pre-Security-Learning-Path---TryHackMe/tree/main/04-%20Fundamentos%20de%20Linux" 
 target="_blank"> Ir al repositorio</a>👈

### **03- Conceptos básicos de explotación de red:** 
Modelo OSI, Encapsulación, El modelo TCP/IP, Herramientas de red (Ping, Traceroute, WHOIS, Dig).

***Nmap***:  
comandos de Nmap, Tipos de escaneos: Escaneos de conexión TCP, Escaneos SYN, Escaneos UDP, Escaneos NULL, FIN 
y Xmas, Escaneo de red ICMP. NSE Scripts: Descripción general, Trabajando con la NSE, Búsqueda de scripts. Evasión de 
firewalls.

***Wireshark:***  
Métodos de recolección (network taps, Mac floods, Envenenamiento ARP), Filtrado de capturas y operadores 
de filtrado (&&, ||, ===, !==, <, >), Disección de paquetes, Tráfico ARP, tráfico ICMP, tráfico TCP, tráfico DNS, 
tráfico HTTP, tráfico HTTPS. Análisis de Exploit PCAP

SMB (enumeración y explotación), Telnet (enumeración y explotación), FTP (enumeración y explotación), NFS (enumeración 
y explotación), SMTP (enumeración y explotación), MySQL (enumeración y explotación)

### **_04- Fundamentos de la piratería web:_**
Como se cargan los sitios web, HTTP (peticiones), cookies, challenge CTF.

***Suite Burp:***  
Funciones, destino, Repeat, challenge. Decoder y Comprarer, Mods, Escáner.

***OWASP Top 10*** : 
1) Inyección, Inyección de comando del sistema operativo, challenge.
2) Pérdida de autenticación, challenge.
3) Exposición de datos confidenciales, challenge.
4) Entidad externa XML, Lenguaje de marcado extensible, Entidad externa XML - DTD, Entidad externa XML - Carga útil XXE,
challenge.
5) Pérdida de Control de Acceso, challenge.
6) Error de configuración de seguridad, challenge.
7) Secuencia de Comandos en Sitios Cruzados, challenge.
8) Deserialización insegura, objetos, deserialización, cookies, ejecucion de codigo.
9) Componentes con vulnerabilidades conocidas,  explotación, challenge.
10) Registro y monitoreo insuficientes.

***Challenge: OWASP Juice Shop*** 

Carga de vulnerabilidades (metodología y sobreescritura de archivos existentes).

***CTF challenge: Pickle Rick***

### **_05- Criptografía:_** 
Hashing, Términos clave, definición y usos de hash, Reconociendo hashes de contraseña, Craqueo de contraseñas, Hash 
para comprobar la integridad.

***John The Ripper:***  
Wordlists, Rompiendo hashes básicos, Rompiendo hashes de autenticación de Windows, Craqueo de hashes de / etc / shadow,
Modo single crack, Reglas personalizadas, Descifrado de archivos zip protegidos con contraseña, Descifrado de archivos 
RAR protegidos con contraseña, Cómo descifrar claves SSH con John.

Cifrado, terminos clave, Criptomatemáticas, Tipos de cifrado (simétrico y asimétrico), RSA (Rivest Shamir Adleman), 
Establecimiento de claves mediante criptografía asimétrica, Firmas digitales y Certificados, Autenticación SSH, 
intercambio de claves de Diffie Hellman, PGP, GPG y AES.

### **_06- Conceptos básicos de explotación de Windows:_** 
Versiones, Sistema de archivos y permisos de Windows, proceso de autenticación (NTLM, LDAP/LDAPS, KERBEROS), 
Herramientas de utilidad incorporadas, tipos de servidores, gestión de usuarios y grupos.
Conceptos básicos de Active Directory, Conceptos básicos de Active Directory, jerarquías de dominio, usuarios y grupos,
Fideicomisos + Políticas,  Servicios de dominio de Active Directory + autenticación, AD en la nube, challenge.

***Metasploit:***   
Comandos, modulos, challenge.

***CTF Challeng: BLUE***

### **_07- Shells y escalada de privilegios:_** 
Definición de Shell, Herramientas, tipos de Shells, Netcat, Estabilización de Shell Netcat, 
Socat,  shells cifradas de Socat, Cargas utiles comunes de Shell, Msfvenom,  Metasploit multi/handler, WebShells. 

***Challenges: Windows Practice Box y Linux Practice Box.***

Privesc común de Linux, dirección de escalada de privilegios, enumeración, Abuso de archivos SUID / GUID, Explotación 
de escritura /etc/passwd, Editor de Vi, Explotando Crontab, Explotación de la variable PATH.

Escalada de privilegios, Linux PrivEsc, Challenges, Exploits de Servicio, Permisos de archivo débiles /etc/shadow 
(legible, escribible), Sudo (secuencias de escape de Shell, variables de entorno), Cron (Permisos de archivo, Variable 
de entorno Path, comodines), Ejecutables SUID/SGID (Exploits conocidos, Inyección de objetos compartidos, Variables de 
entorno, Abuso de las características de Shell), Contraseñas y claves (Archivos de historial, archivos de configuración, 
Claves SSH), NFS, Kernel Exploits, Scripts de escalada de privilegios.


### **_08- CTF: Explotación informática básica:_** 

***CTF: Vulnversity***   
Recopilar informacion con Nmap, Localización de directorios usando GoBuster, Comprometer el servidor web con BurpSuite, 
Escalada de privilegios.

***CTF: Basic Pentesting*** 
Pruebas de aplicaciones web y escalada de privilegios, fuerza bruta, enumeración de servicios, Enumeración de Linux, 
hash cracking.
    
***CTF: Kenobi***
Enumerando Samba para acciones (Nmap), Obtener acceso inicial con ProFtpd (FTP, busqueda de exploits), Escalada de 
privilegios con manipulación de variables de ruta.

***CTF: Steel Mountain***
Acceso inicial, Nmap, busqueda de exploit, Escalada de privilegios, shell inversa, Acceso y escalada sin Metasploit 
(powershell y winPEAS).
