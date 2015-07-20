
#Conmutación y enrutamiento de redes

##Contenido

 * Capitulo 1
 * Capitulo 2
 * Capitulo 3


## Capitulo 1 - Introducción al escalamiento de redes

#### Necesidades de crecimiento de la red
 * Aplicaciones criticas
 * Trafico de redes convergentes
 * Diversas necesidades de negocio
 * Control administrativo centralizado

#### Equipo de clase empresarial
Se instala para proporcionar una red ** Altamente confiable **.

#### Diseño jerarquico de la red
Divide la funcionalidad de la red en tres capas.

##### Capa de acceso
Proporciona conectividad a los usuarios.

##### Capa de distribución
Envia el trafico de una red local a otra.

##### Capa de nucleo
Representa una capa troncal de alta velocidad entre las redes dispersas.

#### Arquitectura empresarial de CISCO
Divide la red en componentes funcionales mientras mantiene las capas de nucleo, acceso y distribución.

Los modulos de la arquitectura empresarial de cisco son.

 * Campus empresarial
 * Perimetro empresarial
 * Perimetro del proveedor de servicios
 * Remoto

![Arquitectura empresarial](http://i.imgur.com/ZPHFLci.png)

##### Campus empresarial
Toda la infraestructura del campues e incluye las capas de acceso, distribución y nucleo.

El módulo de capa de acceso incluye switches de capa 2 o de capa 3 para proporcionar la densidad de puestos requerida.En este módulo se produce la implementación de las VLANs y los enlaces troncales a la capa de distribucion del edificio. La redundancia a los switches de distribución del edificio es importante.

El módulo de distriución agrega acceso al edificio mediante dispositivos de capa 3. En este modulo se llevan a cabo el routing, el control de acceso y el QoS.

El módulo de nucleo proporciona conectividad de alta velocidad entre los módulos de la capa de distribución, las granjas de servidores de los datacenters y el perimetro empresarial.

En este módulo el eje central del diseño es la redundancia, la convergencia rápida y la tolerancia a fallas.

##### Perimetro empresarial
Esta compuesto por los módulos de internet, VPN y WAN que conectan la red de la empresa a la red del proveedor de servicios. Este módulo extiende los servicios de la empresa a sitios remotos y permite que la empresa utilice recursos de internet y de socios.

Proporciona QoS, refuerzo de politicas, niveles de servicio y seguridad.