# Selección del formato y modo de comunicación de incidencias de pedidos

* Status: accepted
* Deciders: Marcos, Blas
* Date: 2023-11-09

Technical Story: RF-8

## Context and Problem Statement

A través de la información sobre las incidencias, el sistema debe de cambiar su comportamiento para adaptarse a las diferentes situaciones que ocurren en tiempo real. ¿Cuál debería ser la información proporcionada al sistema y cómo deberían tratarse internamente las mismas?

## Decision Drivers

* Comunicación más eficiente de incidencias a otros microservicios

## Considered Options

* Comunicación inmediata de incidencia a clase GestorPedidos haciendo uso del patrón Mediator existente y la incorporación de un patrón Observer
* Comunicación periódica de incidencias a GestorPedidos, mediante el agrupamiento y envío de incidencias en un tiempo fijo determinado usando un patrón Composite

## Decision Outcome

Chosen option: "Comunicación inmediata de incidencia a clase GestorPedidos haciendo uso del patrón Mediator existente y la incorporación de un patrón Observer", because comes out best.

### Positive Consequences

* Menor complejidad de acceso y almacenamiento de los datos
* Obtención de información de forma inmediata

### Negative Consequences

* Pérdida de la posibilidad de atención preferente de incidencias prioritarias 

## Pros and Cons of the Options

### Comunicación inmediata de incidencia a clase GestorPedidos haciendo uso del patrón Mediator existente y la incorporación de un patrón Observer

El patrón Observer notificará a GestorPedidos de forma inmediata cuando se produzca una incidencia. GestorPedidos por su parte, haciendo uso de su patrón Mediator, comunicará la información necesaria (principalmente tipo, descripción, prioridad, fecha de generación, estado y comunicador) a las clases que la soliciten

* Good, because Se reutilizan elementos software ya presentes en la arquitectura
* Good, because Se recibe la información de forma inmediata
* Bad, because Posible saturación del sistema como consecuencia de notificaciones continuadas

### Comunicación periódica de incidencias a GestorPedidos, mediante el agrupamiento y envío de incidencias en un tiempo fijo determinado usando un patrón Composite

En cuanto se genere una incidencia, el patrón Composite la clasificará en función de uno o varios criterios (el más importante la prioridad que presente) y la añadirá a su estructura interna en forma de árbol. Transcurrido un tiempo determinado y modificable se enviará esta estructura, junto a los elementos necesarios para el acceso y consulta a cada elemento del árbol, a GestorPedidos, que será capaz de tratar las incidencias ordenadamente siguiendo el criterio seleccionado.

* Good, because Se tratan las incidencias en orden de relevancia
* Good, because Almacenamiento y recopilación de datos de incidencias más preciso y eficaz
* Bad, because Transferencia de información más costosa por la inclusión de métodos para el acceso a la información
* Bad, because Almacenamiento más lento y costoso debido a la clasificación de incidencias
