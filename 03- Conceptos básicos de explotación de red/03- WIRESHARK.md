## Tráfico ARP:

¿Qué es el código de operación para el paquete 6?
 
    Frame 6: 60 bytes on wire (480 bits), 60 bytes captured (480 bits)
    Ethernet II, Src: HuaweiTe_f0:45:d7 (80:fb:06:f0:45:d7), Dst: Sfr_e3:c3:31 (30:7e:cb:e3:c3:31)
    Address Resolution Protocol (request)
        Hardware type: Ethernet (1)
        Protocol type: IPv4 (0x0800)
        Hardware size: 6
        Protocol size: 4
        Opcode: request (1)
        Sender MAC address: HuaweiTe_f0:45:d7 (80:fb:06:f0:45:d7)
        Sender IP address: 10.251.196.1
        Target MAC address: 00:00:00_00:00:00 (00:00:00:00:00:00)
        Target IP address: 10.251.196.227

    request (1)

¿Cuál es la dirección MAC de origen del paquete 19?
 
    Frame 19: 60 bytes on wire (480 bits), 60 bytes captured (480 bits)
    Ethernet II, Src: HuaweiTe_f0:45:d7 (80:fb:06:f0:45:d7), Dst: Sfr_88:e7:a1 (30:7e:cb:88:e7:a1)
    Address Resolution Protocol (request)
        Hardware type: Ethernet (1)
        Protocol type: IPv4 (0x0800)
        Hardware size: 6
        Protocol size: 4
        Opcode: request (1)
        Sender MAC address: HuaweiTe_f0:45:d7 (80:fb:06:f0:45:d7)
        Sender IP address: 10.251.196.1
        Target MAC address: 00:00:00_00:00:00 (00:00:00:00:00:00)
        Target IP address: 10.251.196.74
     

    80:fb:06:f0:45:d7

¿Qué 4 paquetes son paquetes de respuesta?
Se que son respuestas ya que, en la parte de info, no figura la palabra WHO
 
    filtro: arp.opcode == 2
    
    76	61.879614	HuaweiTe_f0:45:d7	Sfr_18:c2:72	ARP	60	10.251.23.1 is at 80:fb:06:f0:45:d7
    400	1388651131.688461	HuaweiTe_f0:45:d7	Sfr_18:c2:72	ARP	60	10.251.23.1 is at 80:fb:06:f0:45:d7
    459	1388651198.798484	HuaweiTe_f0:45:d7	Sfr_18:c2:72	ARP	60	10.251.23.1 is at 80:fb:06:f0:45:d7
    520	1388651266.920150	HuaweiTe_f0:45:d7	Sfr_18:c2:72	ARP	60	10.251.23.1 is at 80:fb:06:f0:45:d7

    76,400,459,520

¿Qué dirección IP está en 80:fb:06:f0:45:d7? Para filtrar, use el siguiente comando: arp contains 80:fb:06:f0:45:d7

    Frame 520: 60 bytes on wire (480 bits), 60 bytes captured (480 bits)
    Ethernet II, Src: HuaweiTe_f0:45:d7 (80:fb:06:f0:45:d7), Dst: Sfr_18:c2:72 (e0:a1:d7:18:c2:72)
    Address Resolution Protocol (reply)
        Hardware type: Ethernet (1)
        Protocol type: IPv4 (0x0800)
        Hardware size: 6
        Protocol size: 4
        Opcode: reply (2)
        Sender MAC address: HuaweiTe_f0:45:d7 (80:fb:06:f0:45:d7)
        Sender IP address: 10.251.23.1
        Target MAC address: Sfr_18:c2:72 (e0:a1:d7:18:c2:72)
        Target IP address: 10.251.23.139
    

    10.251.23.1

## Tráfico ICMP

¿Cuál es el tipo de paquete 4?
 
    Frame 4: 98 bytes on wire (784 bits), 98 bytes captured (784 bits) on interface en1, id 0
    Ethernet II, Src: Apple_13:c5:58 (60:33:4b:13:c5:58), Dst: MS-NLB-PhysServer-26_11:f0:c8:3b (02:1a:11:f0:c8:3b)
    Internet Protocol Version 4, Src: 192.168.43.9, Dst: 8.8.8.8
    Internet Control Message Protocol
        Type: 8 (Echo (ping) request)
        Code: 0
        Checksum: 0xbbb3 [correct]
        [Checksum Status: Good]
        Identifier (BE): 55099 (0xd73b)
        Identifier (LE): 15319 (0x3bd7)
        Sequence Number (BE): 0 (0x0000)
        Sequence Number (LE): 0 (0x0000)
        [Response frame: 5]
        Timestamp from icmp data: May 30, 2013 19:45:17.283108000 Hora estándar de Argentina
        [Timestamp from icmp data (relative): 0.000079000 seconds]
        Data (48 bytes)


    8

¿Cuál es el tipo de paquete 5?
 
    Frame 5: 98 bytes on wire (784 bits), 98 bytes captured (784 bits) on interface en1, id 0
    Ethernet II, Src: MS-NLB-PhysServer-26_11:f0:c8:3b (02:1a:11:f0:c8:3b), Dst: Apple_13:c5:58 (60:33:4b:13:c5:58)
    Internet Protocol Version 4, Src: 8.8.8.8, Dst: 192.168.43.9
    Internet Control Message Protocol
        Type: 0 (Echo (ping) reply)
        Code: 0
        Checksum: 0xc3b3 [correct]
        [Checksum Status: Good]
        Identifier (BE): 55099 (0xd73b)
        Identifier (LE): 15319 (0x3bd7)
        Sequence Number (BE): 0 (0x0000)
        Sequence Number (LE): 0 (0x0000)
        [Request frame: 4]
        [Response time: 492,204 ms]
        Timestamp from icmp data: May 30, 2013 19:45:17.283108000 Hora estándar de Argentina
        [Timestamp from icmp data (relative): 0.492283000 seconds]
        Data (48 bytes)
        

    0

¿Cuál es la marca de tiempo del paquete 12, que solo incluye el día del mes y el año?
nota: Wireshark basa que es el tiempo fuera de la zona horaria de sus dispositivos, si su respuesta es incorrecta, 
intente un día más o menos. 

    Frame 12: 98 bytes on wire (784 bits), 98 bytes captured (784 bits) on interface en1, id 0
    Ethernet II, Src: Apple_13:c5:58 (60:33:4b:13:c5:58), Dst: MS-NLB-PhysServer-26_11:f0:c8:3b (02:1a:11:f0:c8:3b)
    Internet Protocol Version 4, Src: 192.168.43.9, Dst: 8.8.4.4
    Internet Control Message Protocol
        Type: 8 (Echo (ping) request)
        Code: 0
        Checksum: 0x2bfd [correct]
        [Checksum Status: Good]
        Identifier (BE): 56123 (0xdb3b)
        Identifier (LE): 15323 (0x3bdb)
        Sequence Number (BE): 0 (0x0000)
        Sequence Number (LE): 0 (0x0000)
        [No response seen]
        Timestamp from icmp data: May 30, 2013 19:45:20.253336000 Hora estándar de Argentina
        [Timestamp from icmp data (relative): 0.000110000 seconds]
        Data (48 bytes)

 
    may 30,2013

¿Cuál es la cadena de datos completa para el paquete 18? Seleccionar el campo, hacer click derecho> copiar > valor
 
    Frame 18: 98 bytes on wire (784 bits), 98 bytes captured (784 bits) on interface en1, id 0
    Ethernet II, Src: Apple_13:c5:58 (60:33:4b:13:c5:58), Dst: MS-NLB-PhysServer-26_11:f0:c8:3b (02:1a:11:f0:c8:3b)
    Internet Protocol Version 4, Src: 192.168.43.9, Dst: 4.2.2.2
    Internet Control Message Protocol
        Type: 8 (Echo (ping) request)
        Code: 0
        Checksum: 0xb6d2 [correct]
        [Checksum Status: Good]
        Identifier (BE): 56635 (0xdd3b)
        Identifier (LE): 15325 (0x3bdd)
        Sequence Number (BE): 0 (0x0000)
        Sequence Number (LE): 0 (0x0000)
        [Response frame: 19]
        Timestamp from icmp data: May 30, 2013 19:45:24.348349000 Hora estándar de Argentina
        [Timestamp from icmp data (relative): 0.000092000 seconds]
        Data (48 bytes)
            Data: 08090a0b0c0d0e0f101112131415161718191a1b1c1d1e1f202122232425262728292a2b2c2d2e2f3031323334353637
            [Length: 48]


    08090a0b0c0d0e0f101112131415161718191a1b1c1d1e1f202122232425262728292a2b2c2d2e2f3031323334353637

## Tráfico DNS

¿Qué se consulta en el paquete 1?

    Frame 1: 80 bytes on wire (640 bits), 80 bytes captured (640 bits) on interface en1, id 0
    Ethernet II, Src: Apple_13:c5:58 (60:33:4b:13:c5:58), Dst: MS-NLB-PhysServer-26_11:f0:c8:3b (02:1a:11:f0:c8:3b)
    Internet Protocol Version 4, Src: 192.168.43.9, Dst: 192.168.43.1
    User Datagram Protocol, Src Port: 51677, Dst Port: 53
    Domain Name System (query)
        Transaction ID: 0x528e
        Flags: 0x0100 Standard query
        Questions: 1
        Answer RRs: 0
        Authority RRs: 0
        Additional RRs: 0
        Queries
            8.8.8.8.in-addr.arpa: type PTR, class IN


    8.8.8.8.in-addr.arpa

¿Qué sitio se consulta en el paquete 26?

    Frame 26: 77 bytes on wire (616 bits), 77 bytes captured (616 bits) on interface en1, id 0
    Ethernet II, Src: Apple_13:c5:58 (60:33:4b:13:c5:58), Dst: MS-NLB-PhysServer-26_11:f0:c8:3b (02:1a:11:f0:c8:3b)
    Internet Protocol Version 4, Src: 192.168.43.9, Dst: 192.168.43.1
    User Datagram Protocol, Src Port: 54627, Dst Port: 53
    Domain Name System (query)
        Transaction ID: 0x2c58
        Flags: 0x0100 Standard query
        Questions: 1
        Answer RRs: 0
        Authority RRs: 0
        Additional RRs: 0
        Queries
            www.wireshark.org: type A, class IN
        [Response In: 27]


    www.wireshark.org

¿Cuál es el ID de transacción para el paquete 26?

    Frame 26: 77 bytes on wire (616 bits), 77 bytes captured (616 bits) on interface en1, id 0
    Ethernet II, Src: Apple_13:c5:58 (60:33:4b:13:c5:58), Dst: MS-NLB-PhysServer-26_11:f0:c8:3b (02:1a:11:f0:c8:3b)
    Internet Protocol Version 4, Src: 192.168.43.9, Dst: 192.168.43.1
    User Datagram Protocol, Src Port: 54627, Dst Port: 53
    Domain Name System (query)
        Transaction ID: 0x2c58
        Flags: 0x0100 Standard query
        Questions: 1
        Answer RRs: 0
        Authority RRs: 0
        Additional RRs: 0
        Queries
        [Response In: 27]


    0x2c58

## Tráfico HTTP  

¿Qué porcentaje de paquetes se originan en el sistema de nombres de dominio?
Estadisticas-> Jerarquia de protocolos

     - Domain Name System
         - 4.651162790697675
         - 2
         - 0.7692001115937985
         - 193
         - 50.7999947348783
         - 2
         - 193
         - 50.7999947348783
     
    4.7

¿Qué punto final termina en .237?
 
    145.254.160.237

¿Cuál es el agente de usuario listado en el paquete 4?
 
    Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.6) Gecko/20040113

Mirando el flujo de datos, ¿cuál es el URI de solicitud completo del paquete 18?
 
    Frame 4: 533 bytes on wire (4264 bits), 533 bytes captured (4264 bits)
    Ethernet II, Src: Xerox_00:00:00 (00:00:01:00:00:00), Dst: fe:ff:20:00:01:00 (fe:ff:20:00:01:00)
    Internet Protocol Version 4, Src: 145.254.160.237, Dst: 65.208.228.223
    Transmission Control Protocol, Src Port: 3372, Dst Port: 80, Seq: 951057940, Ack: 290218380, Len: 479
    Hypertext Transfer Protocol
        GET /download.html HTTP/1.1\r\n
        Host: www.ethereal.com\r\n
        User-Agent: Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.6) Gecko/20040113\r\n
        Accept: text/xml,application/xml,application/xhtml+xml,text/html;q=0.9,text/plain;q=0.8,image/png,image/jpeg,image/gif;q=0.2,*/*;q=0.1\r\n
        Accept-Language: en-us,en;q=0.5\r\n
        Accept-Encoding: gzip,deflate\r\n
        Accept-Charset: ISO-8859-1,utf-8;q=0.7,*;q=0.7\r\n
        Keep-Alive: 300\r\n
        Connection: keep-alive\r\n
        Referer: http://www.ethereal.com/development.html\r\n
        \r\n
        [Full request URI: http://www.ethereal.com/download.html]
        [HTTP request 1/1]
        [Response in frame: 38]


    http://pagead2.googlesyndication.com/pagead/ads?client=ca-pub-2309191948673629&random=1084443430285&lmt=1082467020&format=468x60_as&output=html&url=http%3A%2F%2Fwww.ethereal.com%2Fdownload.html&color_bg=FFFFFF&color_text=333333&color_link=000000&color_url=666633&color_border=666633

¿Qué nombre de dominio se solicitó del paquete 38?
 
    www.ethereal.com

Mirando el flujo de datos, ¿cuál es el URI de solicitud completo del paquete 38?

    Frame 38: 478 bytes on wire (3824 bits), 478 bytes captured (3824 bits)
    Ethernet II, Src: fe:ff:20:00:01:00 (fe:ff:20:00:01:00), Dst: Xerox_00:00:00 (00:00:01:00:00:00)
    Internet Protocol Version 4, Src: 65.208.228.223, Dst: 145.254.160.237
    Transmission Control Protocol, Src Port: 80, Dst Port: 3372, Seq: 290236320, Ack: 951058419, Len: 424
    [14 Reassembled TCP Segments (18364 bytes): #6(1380), #8(1380), #10(1380), #11(1380), #14(1380), #16(1380), #20(1380), #21(1380), #23(1380), #29(1380), #31(1380), #32(1380), #34(1380), #38(424)]
    Hypertext Transfer Protocol
        HTTP/1.1 200 OK\r\n
        Date: Thu, 13 May 2004 10:17:12 GMT\r\n
        Server: Apache\r\n
        Last-Modified: Tue, 20 Apr 2004 13:17:00 GMT\r\n
        ETag: "9a01a-4696-7e354b00"\r\n
        Accept-Ranges: bytes\r\n
        Content-Length: 18070\r\n
        Keep-Alive: timeout=15, max=100\r\n
        Connection: Keep-Alive\r\n
        Content-Type: text/html; charset=ISO-8859-1\r\n
        \r\n
        [HTTP response 1/1]
        [Time since request: 3.935659000 seconds]
        [Request in frame: 4]
        [Request URI: http://www.ethereal.com/download.html]
        File Data: 18070 bytes
    eXtensible Markup Language


    http://www.ethereal.com/download.html

## Tráfico HTTPS 

Mirando el flujo de datos, ¿cuál es el URI de solicitud completo para el paquete 31?
 
    https://localhost/icons/apache_pb.png

Mirando el flujo de datos, ¿cuál es el URI de solicitud completo para el paquete 50?
 
    https://localhost/icons/back.gif

¿Cuál es el User-Agent listado en el paquete 50?
 
    Mozilla/5.0 (X11; U; Linux i686; fr; rv:1.8.0.2) Gecko/20060308 Firefox/1.5.0.2

