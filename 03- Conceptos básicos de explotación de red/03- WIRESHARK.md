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
 
    8

¿Cuál es el tipo de paquete 5?
 
    0

¿Cuál es la marca de tiempo del paquete 12, que solo incluye el día del mes y el año?
nota: Wireshark basa que es el tiempo fuera de la zona horaria de sus dispositivos, si su respuesta es incorrecta, intente un día más o menos. 
 
    may 30,2013

¿Cuál es la cadena de datos completa para el paquete 18?
Seleccionar el campo, hacer click derecho> copiar > valor
 
    08090a0b0c0d0e0f101112131415161718191a1b1c1d1e1f202122232425262728292a2b2c2d2e2f3031323334353637

## Tráfico DNS

¿Qué se consulta en el paquete 1?
 
    8.8.8.8.in-addr.arpa

¿Qué sitio se consulta en el paquete 26?
 
    www.wireshark.org

¿Cuál es el ID de transacción para el paquete 26?

    0x2c58

## Tráfico HTTP  

¿Qué porcentaje de paquetes se originan en el sistema de nombres de dominio?
 
    4.7

¿Qué punto final termina en .237?
 
    145.254.160.237

¿Cuál es el agente de usuario listado en el paquete 4?
 
    Mozilla/5.0 (Windows; U; Windows NT 5.1; en-US; rv:1.6) Gecko/20040113

Mirando el flujo de datos, ¿cuál es el URI de solicitud completo del paquete 18?
 
    http://pagead2.googlesyndication.com/pagead/ads?client=ca-pub-2309191948673629&random=1084443430285&lmt=1082467020&format=468x60_as&output=html&url=http%3A%2F%2Fwww.ethereal.com%2Fdownload.html&color_bg=FFFFFF&color_text=333333&color_link=000000&color_url=666633&color_border=666633

¿Qué nombre de dominio se solicitó del paquete 38?
 
    www.ethereal.com

Mirando el flujo de datos, ¿cuál es el URI de solicitud completo del paquete 38?

    http://www.ethereal.com/download.html

## Tráfico HTTPS 

Mirando el flujo de datos, ¿cuál es el URI de solicitud completo para el paquete 31?
 
    https://localhost/icons/apache_pb.png

Mirando el flujo de datos, ¿cuál es el URI de solicitud completo para el paquete 50?
 
    https://localhost/icons/back.gif

¿Cuál es el User-Agent listado en el paquete 50?
 
    Mozilla/5.0 (X11; U; Linux i686; fr; rv:1.8.0.2) Gecko/20060308 Firefox/1.5.0.2

