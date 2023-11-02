# Comunicación de microservicios de GestorPedidos

* Status: accepted
* Deciders: Marcos, Blas
* Date: 2023-11-02

Technical Story: RF-2

## Context and Problem Statement

Se necesita definir una forma de comunicación entre los microservicios Clientes, Pedidos, Reparto e Incidencias dentro del paquete GestorPedidos. ¿Qué método es el más adecuado?

## Decision Drivers

* Es más sencillo
* Su funcionamiento no depende el canal de transmisión de datos

## Considered Options

* Patrón Publish-Subscribe
* Patrón Service Discovery
* Patrón Mediator
* Patrón Broker

## Decision Outcome

Chosen option: "Patrón Mediator", because comes out best.

### Positive Consequences

* Mejor comunicación entre los microservicios conectados
* Adaptación de peticiones dentro del propio módulo

### Negative Consequences

* Punto de fallo crítico

## Pros and Cons of the Options

### Patrón Publish-Subscribe

Mientras que un módulo funciona como publicador de información, el otro actúa como suscriptor recogiendo la información depositada en el canal

* Good, because Comunicación asíncrona
* Good, because Canal de comunicación único
* Good, because Mejor transmisión de información a un gran número de microservicios
* Bad, because No válido para microservicios que requieran una interacción cercanas a en tiempo real

### Patrón Service Discovery

Se descubren o eliminan microservicios en función de su estado, generalmente a través de la red

* Good, because Permite el descubrimiento de nuevos microservicios
* Good, because Permite el borrado de microservicios con fallos o latencias altas
* Bad, because Acopla instancias de servicio al Registro de servicios, lo que produce duplicidad

### Patrón Mediator

Se fuerza a los microservicios a colaborar por medio de un componente mediador

* Good, because Ampliamente usado
* Good, because Mayor posibilidad de reutilización de componentes
* Bad, because Más complejo
* Bad, because Añade dependencias entre componentes

### Patrón Broker

Gestiona las solicitudes y comunicaciones entre componentes mediante un componente "broker" que actúa como intermediario entre servicios o componentes distribuidos

* Good, because Gestión de solicitudes en la propia clase
* Good, because Facilita la escalabilidad
* Good, because Los componentes del sistema no necesitan saber los detalles de otros componentes
* Bad, because Facilita la congestión del sistema
* Bad, because Constituye un único punto de fallo
