
# Conceptos basicos de Redes.

## Modelo OSI.

El modelo OSI (Open System Interconnection), desarrollado por la ISO, es un modelo de referencia para los protocolos de la red de arquitectura en capas.

Surgio para hacer frente al problema de la incompatibilidad de las redes basadas en diferentes tecnologias.

El modelo se divide en 7 capas o niveles.
Las capas superiores dependen de capas mas inferiores.

#### 1 Nivel físico.
La primera capa, se encarga de la topologia de red y de las conexiones de la computadora hacia la red. Podemos resumir su funcionalidad de la siguiente manera:
 * Definir el medio o medios físicos por los que va a viajar la comunicación: cable de pares trenzados (o no, como en RS232/EIA232), cable coaxial, guías de onda, aire, fibra óptica.
 * Definir las características materiales (componentes y conectores mecánicos) y eléctricas (niveles de tensión) que se van a usar en la transmisión de los datos por los medios físicos.
 * Definir las características funcionales de la interfaz (establecimiento, mantenimiento y liberación del enlace físico).
 * Transmitir el flujo de bits a través del medio.
 * Manejar las señales eléctricas del medio de transmisión, polos en un enchufe, etc.
 * Garantizar la conexión (aunque no la fiabilidad de dicha conexión).

#### 2. Nivel de enlace de datos.
Esta capa se ocupa del direccionamiento físico, del acceso al medio, de la detección de errores, de la distribución ordenada de tramas y del control del flujo. Es uno de los aspectos más importantes que revisar en el momento de conectar dos ordenadores, ya que está entre la capa 1 y 3 como parte esencial para la creación de sus protocolos básicos (MAC, IP), para regular la forma de la conexión entre computadoras así determinando el paso de tramas (trama = unidad de medida de la información en esta capa, que no es más que la segmentación de los datos trasladándolos por medio de paquetes), verificando su integridad, y corrigiendo errores, por lo cual es importante mantener una excelente adecuación al medio físico (los más usados son el cable UTP, par trenzado o de 8 hilos), con el medio de red que redirecciona las conexiones mediante un router. Dadas estas situaciones cabe recalcar que el dispositivo que usa la capa de enlace es el Switch que se encarga de recibir los datos del router y enviar cada uno de estos a sus respectivos destinatarios (servidor -> computador cliente o algún otro dispositivo que reciba información como teléfonos móviles, tabletas y diferentes dispositivos con acceso a la red, etc.), dada esta situación se determina como el medio que se encarga de la corrección de errores, manejo de tramas, protocolización de datos (se llaman protocolos a las reglas que debe seguir cualquier capa del modelo OSI).

#### 3. Nivel de red.
Se encarga de identificar el enrutamiento existente entre una o más redes. Las unidades de información se denominan paquetes, y se pueden clasificar en protocolos enrutables y protocolos de enrutamiento.
 * Enrutables: viajan con los paquetes (IP, IPX, APPLETALK)
 * Enrutamiento: permiten seleccionar las rutas (RIP, IGRP, EIGRP, OSPF, BGP)

El objetivo de la capa de red es hacer que los datos lleguen desde el origen al destino, aún cuando ambos no estén conectados directamente. Los dispositivos que facilitan tal tarea se denominan encaminadores o enrutadores, aunque es más frecuente encontrarlo con el nombre en inglés routers. Los routers trabajan en esta capa, aunque pueden actuar como switch de nivel 2 en determinados casos, dependiendo de la función que se le asigne. Los firewalls actúan sobre esta capa principalmente, para descartar direcciones de máquinas.
En este nivel se realiza el direccionamiento lógico y la determinación de la ruta de los datos hasta su receptor final.

#### 4. Nivel de transporte.
Capa encargada de efectuar el transporte de los datos (que se encuentran dentro del paquete) de la máquina origen a la de destino, independizándolo del tipo de red física que esté utilizando. La PDU de la capa 4 se llama Segmento o Datagrama, dependiendo de si corresponde a TCP o UDP. Sus protocolos son TCP y UDP; el primero orientado a conexión y el otro sin conexión. Trabajan, por lo tanto, con puertos lógicos y junto con la capa red dan forma a los conocidos como Sockets IP:Puerto (191.16.200.54:80).

#### 5. Nivel de sesióñ
Esta capa es la que se encarga de mantener y controlar el enlace establecido entre dos computadores que están transmitiendo datos de cualquier índole. Por lo tanto, el servicio provisto por esta capa es la capacidad de asegurar que, dada una sesión establecida entre dos máquinas, la misma se pueda efectuar para las operaciones definidas de principio a fin, reanudándolas en caso de interrupción. En muchos casos, los servicios de la capa de sesión son parcial o totalmente prescindibles.

#### 6. Nivel de presentacióñ
El objetivo es encargarse de la representación de la información, de manera que aunque distintos equipos puedan tener diferentes representaciones internas de caracteres los datos lleguen de manera reconocible.
Esta capa es la primera en trabajar más el contenido de la comunicación que el cómo se establece la misma. En ella se tratan aspectos tales como la semántica y la sintaxis de los datos transmitidos, ya que distintas computadoras pueden tener diferentes formas de manejarlas.
Esta capa también permite cifrar los datos y comprimirlos. Por lo tanto, podría decirse que esta capa actúa como un traductor.

#### 7. Nivel de aplicacióñ
Ofrece a las aplicaciones la posibilidad de acceder a los servicios de las demás capas y define los protocolos que utilizan las aplicaciones para intercambiar datos, como correo electrónico (Post Office Protocol y SMTP), gestores de bases de datos y servidor de ficheros (FTP), por UDP pueden viajar (DNS y Routing Information Protocol). Hay tantos protocolos como aplicaciones distintas y puesto que continuamente se desarrollan nuevas aplicaciones el número de protocolos crece sin parar.
Cabe aclarar que el usuario normalmente no interactúa directamente con el nivel de aplicación. Suele interactuar con programas que a su vez interactúan con el nivel de aplicación pero ocultando la complejidad subyacente.

###Regla nemotecnica.
A fin de facilitar el aprendizaje y memorización de los nombres de las capas que componen el modelo; una regla sencilla del BRAPE es memorizarlas como una sigla mnemotécnica: FERTSPA, que en inglés sonaría como First Spa, primer spa en castellano, el cual se define de la siguiente manera:
 * Aplicación
 * Presentación
 * Sesión
 * Transporte
 * Red
 * Enlace de datos
 * Física



















