## El modelo OSI: una descripción general:

¿Qué capa elegiría enviar datos a través de TCP o UDP?

    4- Transporte

¿Qué capa verifica los paquetes recibidos para asegurarse de que no se hayan dañado?

    2- Enlace de Datos

¿En qué capa se formatearían los datos en preparación para la transmisión?

    2- Enlace de Datos

¿Qué capa transmite y recibe datos?

    1- Fisica

¿Qué capa cifra, comprime o transforma los datos iniciales para darles un formato estandarizado?

    6- Presentación

¿Qué capa rastrea las comunicaciones entre el host y las computadoras receptoras?

    5- Sesión

¿Qué capa acepta solicitudes de comunicación de las aplicaciones?

    7- Aplicación

¿Qué capa maneja el direccionamiento lógico?

    3- Red

Al enviar datos a través de TCP , ¿cómo llamaría a los datos "del tamaño de un bocado"?

    Segments

[Investigación] ¿Con qué capa se comunicaría el protocolo FTP ?

    7- Aplicación

¿Qué protocolo de capa de transporte sería el más adecuado para transmitir un video en vivo?

    UDP

## Encapsulación:

¿Cómo se referiría a los datos en la capa 2 del proceso de encapsulación (con el modelo OSI)?

    Frames

¿Cómo se referiría a los datos en la capa 4 del proceso de encapsulación (con el modelo OSI), si se ha seleccionado el protocolo UDP ?

    Datagrams

¿Qué proceso realizaría una computadora en un mensaje recibido?

    De-encapsulation

¿Cuál es la única capa del modelo OSI que agrega un tráiler  durante la encapsulación?

    Data Link

¿La encapsulación proporciona una capa adicional de seguridad (Sí/No) ?

    Yes

## El modelo TCP/IP:

¿Qué modelo se introdujo primero, OSI o TCP/IP?

    TCP/IP

¿Qué capa del modelo TCP/IP cubre la funcionalidad de la capa de transporte del modelo OSI (Nombre completo) ?

    Transport

¿Qué capa del modelo TCP/IP cubre la funcionalidad de la capa de sesión del modelo OSI (Nombre completo) ?

    Application

La capa de interfaz de red del modelo TCP/IP cubre la funcionalidad de dos capas en el modelo OSI. Estas capas son Data Link y?.. (Nombre completo) ?

    Physical

¿Qué capa del modelo TCP/IP maneja la funcionalidad de la capa de red OSI?

    Internet

¿Qué tipo de protocolo es TCP?

    Connection-based

¿Qué significa SYN?

    Synchronise

¿Cuál es el segundo paso del apretón de manos de tres vías?

    SYN/ACK

¿Cuál es el nombre abreviado del segmento "Reconocimiento" en el apretón de manos de tres vías?

    ACK

## Herramientas de red: PING

¿Qué comando usaría para hacer ping al sitio web bbc.co.uk?

    cisco@labvm:~$ ping bbc.co.uk

Ping muirlandoracle.co.uk ¿Cuál es la dirección IPv4?

    cisco@labvm:~$ ping muirlandoracle.co.uk
    PING muirlandoracle.co.uk (217.160.0.152) 56(84) bytes of data.
    64 bytes from 217-160-0-152.elastic-ssl.ui-r.com (217.160.0.152): icmp_seq=1 ttl=52 time=252 ms
    64 bytes from 217-160-0-152.elastic-ssl.ui-r.com (217.160.0.152): icmp_seq=2 ttl=52 time=252 ms
    64 bytes from 217-160-0-152.elastic-ssl.ui-r.com (217.160.0.152): icmp_seq=3 ttl=52 time=254 ms
    ^C
    --- muirlandoracle.co.uk ping statistics ---
    3 packets transmitted, 3 received, 0% packet loss, time 2012ms
    rtt min/avg/max/mdev = 251.815/252.704/253.995/0.934 m
        
    217.160.0.152

¿Qué interruptor le permite cambiar el intervalo de las solicitudes de ping enviadas?

    cisco@labvm:~$ man ping

    -i interval
           Wait interval seconds between sending each packet. The default is to wait for one
           second between each packet normally, or not to wait in flood mode. Only super-user
           may set interval to values less than 0.2 seconds.

¿Qué conmutador le permitiría restringir las solicitudes a IPv4?

    cisco@labvm:~$ man ping
    
    -4
               Use IPv4 only.

¿Qué interruptor le daría una salida más detallada?

    cisco@labvm:~$ man ping

    -v
           Verbose output.

## Herramientas de red: TRACEROUTE

Usa traceroute en tryhackme.com ¿Puedes ver la ruta que ha tomado tu solicitud?

    Ejemplo con windows:    

    C:\Users\Manu>tracert tryhackme.com
    
    Traza a la dirección tryhackme.com [104.22.54.228]
    sobre un máximo de 30 saltos:
    
      1    <1 ms    <1 ms    <1 ms  192.168.0.1
      2     *        *        *     Tiempo de espera agotado para esta solicitud.
      3     *        *        *     Tiempo de espera agotado para esta solicitud.
      4    18 ms    18 ms    18 ms  host192.181-89-3.telecom.net.ar [181.89.3.192]
      5     *        *        *     Tiempo de espera agotado para esta solicitud.
      6     *        *        *     Tiempo de espera agotado para esta solicitud.
      7    27 ms    20 ms    24 ms  ae13.baires3.bai.seabone.net [195.22.220.56]
      8    18 ms    18 ms    23 ms  ae8.baires5.bai.seabone.net [195.22.220.119]
      9    26 ms    20 ms    20 ms  cloudflare.baires5.bai.seabone.net [185.70.203.71]
     10    20 ms    19 ms    19 ms  104.22.54.228
    
    Traza completa.


¿Qué interruptor usaría para especificar una interfaz al usar Traceroute?

    -i

¿Qué interruptor usaría si quisiera usar solicitudes TCP SYN al rastrear la ruta?

    -T

[Pensamiento lateral]  ¿En qué capa del modelo TCP/IP se ejecutará traceroute de forma predeterminada (Windows)?

    Internet

## Herramientas de red: WHOIS

Realice una búsqueda whois en facebook.com

    cisco@labvm:~$ whois facebook.com
       Domain Name: FACEBOOK.COM
       Registry Domain ID: 2320948_DOMAIN_COM-VRSN
       Registrar WHOIS Server: whois.registrarsafe.com
       Registrar URL: http://www.registrarsafe.com
       Updated Date: 2022-01-26T16:45:06Z
       Creation Date: 1997-03-29T05:00:00Z
       Registry Expiry Date: 2031-03-30T04:00:00Z
       Registrar: RegistrarSafe, LLC
       Registrar IANA ID: 3237
       Registrar Abuse Contact Email: abusecomplaints@registrarsafe.com
       Registrar Abuse Contact Phone: +1-650-308-7004
       Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
       Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
       Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
       Domain Status: serverDeleteProhibited https://icann.org/epp#serverDeleteProhibited
       Domain Status: serverTransferProhibited https://icann.org/epp#serverTransferProhibited
       Domain Status: serverUpdateProhibited https://icann.org/epp#serverUpdateProhibited
       Name Server: A.NS.FACEBOOK.COM
       Name Server: B.NS.FACEBOOK.COM
       Name Server: C.NS.FACEBOOK.COM
       Name Server: D.NS.FACEBOOK.COM
       DNSSEC: unsigned
       URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
    >>> Last update of whois database: 2022-02-12T08:22:23Z <<<
    
    For more information on Whois status codes, please visit https://icann.org/epp
    
    NOTICE: The expiration date displayed in this record is the date the
    registrar's sponsorship of the domain name registration in the registry is
    currently set to expire. This date does not necessarily reflect the expiration
    date of the domain name registrant's agreement with the sponsoring
    registrar.  Users may consult the sponsoring registrar's Whois database to
    view the registrar's reported date of expiration for this registration.
    
    TERMS OF USE: You are not authorized to access or query our Whois
    database through the use of electronic processes that are high-volume and
    automated except as reasonably necessary to register domain names or
    modify existing registrations; the Data in VeriSign Global Registry
    Services' ("VeriSign") Whois database is provided by VeriSign for
    information purposes only, and to assist persons in obtaining information
    about or related to a domain name registration record. VeriSign does not
    guarantee its accuracy. By submitting a Whois query, you agree to abide
    by the following terms of use: You agree that you may use this Data only
    for lawful purposes and that under no circumstances will you use this Data
    to: (1) allow, enable, or otherwise support the transmission of mass
    unsolicited, commercial advertising or solicitations via e-mail, telephone,
    or facsimile; or (2) enable high volume, automated, electronic processes
    that apply to VeriSign (or its computer systems). The compilation,
    repackaging, dissemination or other use of this Data is expressly
    prohibited without the prior written consent of VeriSign. You agree not to
    use electronic processes that are automated and high-volume to access or
    query the Whois database except as reasonably necessary to register
    domain names or modify existing registrations. VeriSign reserves the right
    to restrict your access to the Whois database in its sole discretion to ensure
    operational stability.  VeriSign may restrict or terminate your access to the
    Whois database for failure to abide by these terms of use. VeriSign
    reserves the right to modify these terms at any time.
    
    The Registry database contains ONLY .COM, .NET, .EDU domains and
    Registrars.
    Domain Name: FACEBOOK.COM
    Registry Domain ID: 2320948_DOMAIN_COM-VRSN
    Registrar WHOIS Server: whois.registrarsafe.com
    Registrar URL: https://www.registrarsafe.com
    Updated Date: 2022-01-26T16:45:06Z
    Creation Date: 1997-03-29T05:00:00Z
    Registrar Registration Expiration Date: 2031-03-30T04:00:00Z
    Registrar: RegistrarSafe, LLC
    Registrar IANA ID: 3237
    Registrar Abuse Contact Email: abusecomplaints@registrarsafe.com
    Registrar Abuse Contact Phone: +1.6503087004
    Domain Status: serverUpdateProhibited https://www.icann.org/epp#serverUpdateProhibited
    Domain Status: clientDeleteProhibited https://www.icann.org/epp#clientDeleteProhibited
    Domain Status: clientTransferProhibited https://www.icann.org/epp#clientTransferProhibited
    Domain Status: serverDeleteProhibited https://www.icann.org/epp#serverDeleteProhibited
    Domain Status: serverTransferProhibited https://www.icann.org/epp#serverTransferProhibited
    Domain Status: clientUpdateProhibited https://www.icann.org/epp#clientUpdateProhibited
    Registry Registrant ID: 
    Registrant Name: Domain Admin
    Registrant Organization: Meta Platforms, Inc.
    Registrant Street: 1601 Willow Rd 
    Registrant City: Menlo Park
    Registrant State/Province: CA
    Registrant Postal Code: 94025
    Registrant Country: US
    Registrant Phone: +1.6505434800
    Registrant Phone Ext:
    Registrant Fax: +1.6505434800
    Registrant Fax Ext:
    Registrant Email: domain@fb.com
    Registry Admin ID: 
    Admin Name: Domain Admin
    Admin Organization: Meta Platforms, Inc.
    Admin Street: 1601 Willow Rd 
    Admin City: Menlo Park
    Admin State/Province: CA
    Admin Postal Code: 94025
    Admin Country: US
    Admin Phone: +1.6505434800
    Admin Phone Ext:
    Admin Fax: +1.6505434800
    Admin Fax Ext:
    Admin Email: domain@fb.com
    Registry Tech ID: 
    Tech Name: Domain Admin
    Tech Organization: Meta Platforms, Inc.
    Tech Street: 1601 Willow Rd 
    Tech City: Menlo Park
    Tech State/Province: CA
    Tech Postal Code: 94025
    Tech Country: US
    Tech Phone: +1.6505434800
    Tech Phone Ext:
    Tech Fax: +1.6505434800
    Tech Fax Ext:
    Tech Email: domain@fb.com
    Name Server: C.NS.FACEBOOK.COM
    Name Server: B.NS.FACEBOOK.COM
    Name Server: A.NS.FACEBOOK.COM
    Name Server: D.NS.FACEBOOK.COM
    DNSSEC: unsigned
    URL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/
    >>> Last update of WHOIS database: 2022-02-12T19:23:51Z <<<
    
    Search results obtained from the RegistrarSafe, LLC WHOIS database are
    provided by RegistrarSafe, LLC for information purposes only, to assist
    users in obtaining information concerning a domain name registration record.
    The information contained therein is provided on an "as is" and "as available"
    basis and RegistrarSafe, LLC does not guarantee the accuracy or completeness
    of any information provided through the WHOIS database.  By submitting a WHOIS query,
    you agree to the following: (1) that you will use any information provided through
    the WHOIS only for lawful purposes; (2) that you will comply with all ICANN rules
    and regulations governing use of the WHOIS; (3)  that you will not use any information
    provided through the WHOIS to  enable, or otherwise cause the transmission of mass
    unsolicited, commercial advertising or solicitations via e-mail (i.e., spam); or
    (4) that you will not use the WHOIS to enable or otherwise utilize high volume,
    automated, electronic processes that apply to or attach to RegistrarSafe, LLC or
    its systems. RegistrarSafe, LLC reserves the right to modify these terms
    at any time and to take any other appropriate actions, including but not limited to
    restricting any access that violates these terms and conditions. By submitting this
    query, you acknowledge and agree to abide by the foregoing terms, conditions and policies.
    
    For more information on Whois status codes, please visit
        https://www.icann.org/resources/pages/epp-status-codes-2014-06-16-en.


¿Cuál es el código postal del registrante de facebook.com?

    Registrant Postal Code: 94025

¿Cuándo se registró por primera vez el dominio facebook.com (formato: DD/MM/AAAA)?

    Creation Date: 1997-03-29T05:00:00Z    
    29/03/1997

Realice una búsqueda whois en microsoft.com

    cisco@labvm:~$ whois microsoft.com
       Domain Name: MICROSOFT.COM
       Registry Domain ID: 2724960_DOMAIN_COM-VRSN
       Registrar WHOIS Server: whois.markmonitor.com
       Registrar URL: http://www.markmonitor.com
       Updated Date: 2021-03-12T23:25:32Z
       Creation Date: 1991-05-02T04:00:00Z
       Registry Expiry Date: 2022-05-03T04:00:00Z
       Registrar: MarkMonitor Inc.
       Registrar IANA ID: 292
       Registrar Abuse Contact Email: abusecomplaints@markmonitor.com
       Registrar Abuse Contact Phone: +1.2083895740
       Domain Status: clientDeleteProhibited https://icann.org/epp#clientDeleteProhibited
       Domain Status: clientTransferProhibited https://icann.org/epp#clientTransferProhibited
       Domain Status: clientUpdateProhibited https://icann.org/epp#clientUpdateProhibited
       Domain Status: serverDeleteProhibited https://icann.org/epp#serverDeleteProhibited
       Domain Status: serverTransferProhibited https://icann.org/epp#serverTransferProhibited
       Domain Status: serverUpdateProhibited https://icann.org/epp#serverUpdateProhibited
       Name Server: NS1-205.AZURE-DNS.COM
       Name Server: NS2-205.AZURE-DNS.NET
       Name Server: NS3-205.AZURE-DNS.ORG
       Name Server: NS4-205.AZURE-DNS.INFO
       DNSSEC: unsigned
       URL of the ICANN Whois Inaccuracy Complaint Form: https://www.icann.org/wicf/
    >>> Last update of whois database: 2022-02-12T07:24:36Z <<<
    
    For more information on Whois status codes, please visit https://icann.org/epp
    
    NOTICE: The expiration date displayed in this record is the date the
    registrar's sponsorship of the domain name registration in the registry is
    currently set to expire. This date does not necessarily reflect the expiration
    date of the domain name registrant's agreement with the sponsoring
    registrar.  Users may consult the sponsoring registrar's Whois database to
    view the registrar's reported date of expiration for this registration.
    
    TERMS OF USE: You are not authorized to access or query our Whois
    database through the use of electronic processes that are high-volume and
    automated except as reasonably necessary to register domain names or
    modify existing registrations; the Data in VeriSign Global Registry
    Services' ("VeriSign") Whois database is provided by VeriSign for
    information purposes only, and to assist persons in obtaining information
    about or related to a domain name registration record. VeriSign does not
    guarantee its accuracy. By submitting a Whois query, you agree to abide
    by the following terms of use: You agree that you may use this Data only
    for lawful purposes and that under no circumstances will you use this Data
    to: (1) allow, enable, or otherwise support the transmission of mass
    unsolicited, commercial advertising or solicitations via e-mail, telephone,
    or facsimile; or (2) enable high volume, automated, electronic processes
    that apply to VeriSign (or its computer systems). The compilation,
    repackaging, dissemination or other use of this Data is expressly
    prohibited without the prior written consent of VeriSign. You agree not to
    use electronic processes that are automated and high-volume to access or
    query the Whois database except as reasonably necessary to register
    domain names or modify existing registrations. VeriSign reserves the right
    to restrict your access to the Whois database in its sole discretion to ensure
    operational stability.  VeriSign may restrict or terminate your access to the
    Whois database for failure to abide by these terms of use. VeriSign
    reserves the right to modify these terms at any time.
    
    The Registry database contains ONLY .COM, .NET, .EDU domains and
    Registrars.
    Domain Name: microsoft.com
    Registry Domain ID: 2724960_DOMAIN_COM-VRSN
    Registrar WHOIS Server: whois.markmonitor.com
    Registrar URL: http://www.markmonitor.com
    Updated Date: 2021-04-07T19:58:15+0000
    Creation Date: 1991-05-02T04:00:00+0000
    Registrar Registration Expiration Date: 2022-05-02T07:00:00+0000
    Registrar: MarkMonitor, Inc.
    Registrar IANA ID: 292
    Registrar Abuse Contact Email: abusecomplaints@markmonitor.com
    Registrar Abuse Contact Phone: +1.2083895770
    Domain Status: clientUpdateProhibited (https://www.icann.org/epp#clientUpdateProhibited)
    Domain Status: clientTransferProhibited (https://www.icann.org/epp#clientTransferProhibited)
    Domain Status: clientDeleteProhibited (https://www.icann.org/epp#clientDeleteProhibited)
    Domain Status: serverUpdateProhibited (https://www.icann.org/epp#serverUpdateProhibited)
    Domain Status: serverTransferProhibited (https://www.icann.org/epp#serverTransferProhibited)
    Domain Status: serverDeleteProhibited (https://www.icann.org/epp#serverDeleteProhibited)
    Registry Registrant ID: 
    Registrant Name: Domain Administrator
    Registrant Organization: Microsoft Corporation
    Registrant Street: One Microsoft Way, 
    Registrant City: Redmond
    Registrant State/Province: WA
    Registrant Postal Code: 98052
    Registrant Country: US
    Registrant Phone: +1.4258828080
    Registrant Phone Ext: 
    Registrant Fax: +1.4259367329
    Registrant Fax Ext: 
    Registrant Email: admin@domains.microsoft
    Registry Admin ID: 
    Admin Name: Domain Administrator
    Admin Organization: Microsoft Corporation
    Admin Street: One Microsoft Way, 
    Admin City: Redmond
    Admin State/Province: WA
    Admin Postal Code: 98052
    Admin Country: US
    Admin Phone: +1.4258828080
    Admin Phone Ext: 
    Admin Fax: +1.4259367329
    Admin Fax Ext: 
    Admin Email: admin@domains.microsoft
    Registry Tech ID: 
    Tech Name: MSN Hostmaster
    Tech Organization: Microsoft Corporation
    Tech Street: One Microsoft Way, 
    Tech City: Redmond
    Tech State/Province: WA
    Tech Postal Code: 98052
    Tech Country: US
    Tech Phone: +1.4258828080
    Tech Phone Ext: 
    Tech Fax: +1.4259367329
    Tech Fax Ext: 
    Tech Email: msnhst@microsoft.com
    Name Server: ns4-205.azure-dns.info
    Name Server: ns3-205.azure-dns.org
    Name Server: ns1-205.azure-dns.com
    Name Server: ns2-205.azure-dns.net
    DNSSEC: unsigned
    URL of the ICANN WHOIS Data Problem Reporting System: http://wdprs.internic.net/
    >>> Last update of WHOIS database: 2022-02-12T19:21:48+0000 <<<
    
    For more information on WHOIS status codes, please visit:
      https://www.icann.org/resources/pages/epp-status-codes
    
    If you wish to contact this domain’s Registrant, Administrative, or Technical
    contact, and such email address is not visible above, you may do so via our web
    form, pursuant to ICANN’s Temporary Specification. To verify that you are not a
    robot, please enter your email address to receive a link to a page that
    facilitates email communication with the relevant contact(s).
    
    Web-based WHOIS:
      https://domains.markmonitor.com/whois
    
    If you have a legitimate interest in viewing the non-public WHOIS details, send
    your request and the reasons for your request to whoisrequest@markmonitor.com
    and specify the domain name in the subject line. We will review that request and
    may ask for supporting documentation and explanation.
    
    The data in MarkMonitor’s WHOIS database is provided for information purposes,
    and to assist persons in obtaining information about or related to a domain
    name’s registration record. While MarkMonitor believes the data to be accurate,
    the data is provided "as is" with no guarantee or warranties regarding its
    accuracy.
    
    By submitting a WHOIS query, you agree that you will use this data only for
    lawful purposes and that, under no circumstances will you use this data to:
      (1) allow, enable, or otherwise support the transmission by email, telephone,
    or facsimile of mass, unsolicited, commercial advertising, or spam; or
      (2) enable high volume, automated, or electronic processes that send queries,
    data, or email to MarkMonitor (or its systems) or the domain name contacts (or
    its systems).
    
    MarkMonitor reserves the right to modify these terms at any time.
    
    By submitting this query, you agree to abide by this policy.
    
    MarkMonitor Domain Management(TM)
    Protecting companies and consumers in a digital world.
    
    Visit MarkMonitor at https://www.markmonitor.com
    Contact us at +1.8007459229
    In Europe, at +44.02032062220
    ----

¿En qué ciudad se encuentra el registrante?

    Registrant City: Redmond

[OSINT] ¿Cuál es el nombre del campo de golf que está cerca de la dirección de registro de microsoft.com?

    Bellevue Golf Course

¿Cuál es el correo electrónico técnico registrado para microsoft.com?

    Tech Email: msnhst@microsoft.com

## Herramientas de red: DIG

¿Qué significa DNS ?

    Domain Name System

¿Cuál es el primer tipo de servidor DNS que su computadora consultaría cuando busca un dominio?

    Recursive

¿Qué tipo de servidor DNS contiene registros específicos de extensiones de dominio (es decir , .com, .co.uk*, etc.)*? Utilice la versión larga del nombre.

    Top-Level Domain

¿Cuál es el primer lugar donde buscaría su computadora para encontrar la dirección IP de un dominio?

    Local Cache

[Investigación]  Google ejecuta dos servidores DNS públicos. Uno de ellos se puede consultar con la IP 8.8.8.8, 
¿cuál es la dirección IP del otro?

    8.8.4.4

    cisco@labvm:~$ dig google.com @8.8.4.4
    
    ; <<>> DiG 9.16.1-Ubuntu <<>> google.com @8.8.4.4
    ;; global options: +cmd
    ;; Got answer:
    ;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 17325
    ;; flags: qr rd ra; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1
    
    ;; OPT PSEUDOSECTION:
    ; EDNS: version: 0, flags:; udp: 512
    ;; QUESTION SECTION:
    ;google.com.			IN	A
    
    ;; ANSWER SECTION:
    google.com.		251	IN	A	142.250.79.142
    
    ;; Query time: 20 msec
    ;; SERVER: 8.8.4.4#53(8.8.4.4)
    ;; WHEN: Sat Feb 12 19:40:05 UTC 2022
    ;; MSG SIZE  rcvd: 55


Si una consulta de DNS tiene un TTL de 24 horas, ¿qué número mostraría la consulta de excavación?

    86400
