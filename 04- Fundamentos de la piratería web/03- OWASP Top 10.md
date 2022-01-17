## [Severity 1] Command Injection Practical

¿Qué archivo de texto extraño se encuentra en el directorio raíz del sitio web?
 
    drpeper.txt
 
¿Cuántos usuarios no root / no de servicio / no demonio hay?
 
    0

¿Con qué usuario se ejecuta esta aplicación?
 
    www-data 

¿Cómo está configurado el shell del usuario?
 
    /usr/sbin/nologin 

¿Qué versión de Ubuntu se está ejecutando?
 
    18.04.4
 
Imprime el MOTD. ¿Qué bebida favorita se muestra?
 
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


