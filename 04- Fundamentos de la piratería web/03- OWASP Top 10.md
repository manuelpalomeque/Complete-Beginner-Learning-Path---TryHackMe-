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
