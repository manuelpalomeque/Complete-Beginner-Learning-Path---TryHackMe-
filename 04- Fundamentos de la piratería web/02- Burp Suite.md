## Resumen de Funciones:

¿Qué herramienta de Burp Suite podemos usar para realizar una 'diferencia'(diff) en las respuestas y otros datos?
 
    Comparer 

¿Qué herramienta podríamos usar para analizar la aleatoriedad en diferentes datos, como los tokens de restablecimiento de contraseña?
 
    Sequencer 

¿Qué herramienta podemos utilizar para establecer el alcance de nuestro proyecto?
 
    Target 

Si bien solo está disponible en las versiones premium de Burp Suite, ¿qué herramienta podemos usar para identificar automáticamente diferentes vulnerabilidades en la aplicación que estamos examinando?
 
    Scanner 

Codificar o decodificar datos puede ser particularmente útil cuando se examinan los parámetros de URL o las protecciones en un formulario, ¿qué herramienta nos permite hacer precisamente eso?
 
    Decoder 

¿Qué herramienta nos permite redirigir nuestro tráfico web a Burp para un examen más detallado?
 
    Proxy 

Simple en concepto pero potente en ejecución, ¿qué herramienta nos permite volver a emitir solicitudes?
 
    Repeater 

Con cuatro modos, ¿qué herramienta en Burp podemos usar para una variedad de propósitos, como el campo fuzzing?
 
    Extender 

Por último, pero no menos importante, ¿qué herramienta nos permite modificar Burp Suite mediante la adición de extensiones?
 
    Extender 

## Proxy

De forma predeterminada, el proxy Burp Suite escucha en una sola interfaz. ¿Qué es? Utilice el formato de IP: PUERTO
 
    127.0.0.1:8080

Regrese a su navegador web y navegue hasta la aplicación web alojada en la máquina virtual que implementamos hace un 
momento. Tenga en cuenta que la página parece cargarse continuamente. Regrese a Burp Suite, ahora tenemos una solicitud 
que está esperando en nuestra pestaña de intercepción. Eche un vistazo a las acciones, ¿qué atajo nos permite reenviar 
la solicitud al repetidor?

    Ctrl-R

¿Qué tal si quisiéramos enviar nuestra solicitud a Intruder?

    Ctrl-I

Burp Suite guarda el historial de solicitudes enviadas a través del proxy junto con sus diferentes detalles. Esto puede
ser especialmente útil cuando necesitamos tener pruebas de nuestras acciones durante una prueba de penetración o 
queremos modificar y reenviar una solicitud que enviamos hace un tiempo. ¿Cuál es el nombre de la primera sección en la 
que se guardan las solicitudes web generales (GET / POST)?

    HTTP history

Definido en RFC 6455 como un protocolo de comunicación de baja latencia que no requiere encapsulación HTTP, ¿cuál es el 
nombre de la segunda sección de nuestro historial guardado en Burp Suite? Estos se usan comúnmente en aplicaciones de 
colaboración que requieren actualizaciones en tiempo real (Google Docs es un excelente ejemplo aquí).
 
    WebSockets history

Antes de pasar a explorar nuestra definición de destino, echemos un vistazo a algunas de las personalizaciones avanzadas 
que podemos utilizar en el proxy Burp. Vaya a la sección Opciones de la pestaña Proxy y desplácese hacia abajo hasta 
Interceptar solicitudes de clientes. Aquí podemos aplicar más reglas detalladas para definir qué solicitudes nos 
gustaría interceptar. Quizás la más útil de las reglas predeterminadas es nuestra única regla AND. ¿Cuál es su tipo de 
concordancia?
 
    URL

¿Qué tal es 'Relación'? En esta situación, habilitar esta regla de coincidencia puede ser increíblemente útil después 
de la definición del objetivo, ya que podemos dejar la intercepción de forma permanente (a menos que necesitemos 
navegar sin interceptar) ya que no perturbará los sitios que están fuera de nuestro alcance, algo que es particularmente
bueno si necesitamos algo en Google en el mismo navegador.

    is in target scope

## Definición de destino

Navegue por el resto de la aplicación para construir nuestra estructura de página en la pestaña de destino. Una vez que 
haya visitado la mayoría de las páginas del sitio, regrese a Burp Suite y expanda los distintos niveles del directorio 
de la aplicación. ¿Cómo llamamos a esta representación de la aplicación web colectiva?

    site map

¿Cuál es el término para navegar por la aplicación como un usuario normal antes de examinarla más a fondo?

    happy path

Las definiciones de problemas que se encuentran aquí son cómo Burp Suite define los problemas dentro de los informes. 
Al comenzar, estas definiciones de problemas pueden ser particularmente útiles para comprender y categorizar varios 
hallazgos que podamos tener. ¿Qué problema de envenenamiento surge cuando una aplicación detrás de una entrada de 
proceso de caché no está incluida en la clave de caché?

    web cache poisoning

## Poniéndolo en Repeat [er]

Para comenzar, haga clic en 'Cuenta' (esto podría ser 'Iniciar sesión' según la versión de Juice Shop) en la esquina 
superior derecha de Juice Shop para navegar a la página de inicio de sesión.

    En el navegador ir a la dirección IP de la maquina virtual para que abra la pagina 10.10.82.71
    http://10.10.82.71/#/login

Intente iniciar sesión con credenciales no válidas. ¿Qué error se genera cuando falla el inicio de sesión?

    Invalid email or password

Ahora que hemos enviado la solicitud a Repeater, intentemos ajustar la solicitud de modo que enviemos una sola 
cotización (') como correo electrónico y contraseña. ¿Qué error se genera a partir de esta solicitud?

    Cambiar a pestaña Repeater
    Cambiar el usuario yo la clave y poner un “’”
    Hacer click en send

    SQLITE_ERROR

¿Qué campo tenemos que modificar para enviar una revisión de cero estrellas?

    rating

## ¡Ayudar! ¡Hay un intruso!

¿Qué tipo de ataque nos permite seleccionar múltiples conjuntos de cargas útiles (uno por posición) e iterar a través 
de ellos simultáneamente?

    Pitchfork 

¿Qué tal el tipo de ataque que nos permite usar un conjunto de carga útil en cada posición que hemos seleccionado 
simultáneamente?

    Battering Ram

¿Qué tipo de ataque nos permite seleccionar múltiples conjuntos de carga útil (uno por posición) e iterar a través de 
todas las combinaciones posibles?

    Cluster Bomb

Quizás el más utilizado, ¿qué tipo de ataque nos permite recorrer nuestro conjunto de cargas útiles,  colocando la 
siguiente carga útil disponible en cada posición a su vez?

    Sniper

Finalmente, haga clic en 'Iniciar ataque'. ¿Cuál es la primera carga útil que devuelve un código de estado 200, que 
muestra que hemos omitido con éxito la autenticación?

    a' or 1=1--

## Resulta que las máquinas son mejores en matemáticas que nosotros

Analiza los resultados. ¿En qué se mide la entropía estimada efectiva?

    bits

Para encontrar los bits utilizables de entropía, a menudo tenemos que hacer algunos ajustes para tener un conjunto de 
datos normalizado. ¿Qué artículo se convierte en este proceso?

    token

##  Decodificador y comparador

¿Con qué carácter se decodifica el% 20 en la solicitud que copiamos en Decoder

    space

Al igual que CyberChef, Decoder también tiene un modo "Mágico" en el que intentará decodificar automáticamente la 
entrada que se le proporcione. ¿Cómo se llama este modo? 

    smart decode

¿Qué podemos cargar en Comparer para ver las diferencias en los distintos roles de usuario a los que pueden acceder? 
Esto es muy útil para verificar problemas de control de acceso.

    site maps

Comparer puede realizar una diferencia contra dos métricas diferentes, ¿cuál nos permite examinar los datos cargados 
como están en lugar de dividirlos en bytes?

    words

