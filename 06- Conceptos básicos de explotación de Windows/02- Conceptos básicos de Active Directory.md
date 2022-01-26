## Almacén de datos de AD DS 

¿Qué base de datos contiene AD DS? ntds.dit
 
    ntds.dit
 
¿Dónde se almacena NTDS.dit?
 
    %SystemRoot%\NTDS

¿Qué tipo de máquina puede ser un controlador de dominio?

    windows server

## the Forest

¿Cuál es el término para una  jerarquía de dominios en una red?
 
    tree
 
¿Cuál es el término para las reglas para la creación de objetos?
 
    domain schema
 
¿Cuál es el término para contenedores para grupos, computadoras, usuarios, impresoras y otras unidades organizativas?
    
    Organizational Units

## Resumen de grupos 

¿Qué tipo de grupos especifican permisos de usuario?
 
    security groups
 
¿Qué grupo contiene todas las estaciones de trabajo y servidores unidos al dominio?
 
    domain computers
 
¿Qué grupo puede publicar certificados en el directorio?
 
    cert publishers

¿Qué usuario puede realizar cambios en una máquina local pero no en un controlador de dominio?
 
    local administratos
 
¿Qué grupo tiene sus contraseñas replicadas en controladores de dominio de solo lectura?

    Allowed RODC Password Replication Group

## Fideicomisos + Políticas 

¿Qué tipo de confianza fluye de un dominio de confianza a un dominio de confianza?
 
    directional

¿Qué tipo de fideicomisos se expande para incluir otros dominios de confianza?

    transitive

## Servicios de dominio de Active Directory + autenticación

¿Qué tipo de autenticación utiliza tickets? 
 
    kerberos

¿Qué servicio de dominio puede crear, validar y revocar certificados de clave pública?
 
    certificate services

## AD en la nube

¿Cuál es el equivalente en Azure AD de LDAP?
 
    Rest APIs

¿Cuál es el equivalente de Azure AD a Domains and Forests?
 
    Tenants

¿Cuál es el equivalente de Windows Server AD de los invitados?
 
    Trusts