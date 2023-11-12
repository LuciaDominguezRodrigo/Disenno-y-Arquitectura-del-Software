# Selección del estilo de la arquitectura

* Status: accepted
* Deciders: 2
* Date: 2023-10-19

Technical Story: RF-1.2

## Context and Problem Statement

Se requiere un sistema con arquitectura orientada a microservicios, que sea flexible, modular y fácilmente expandible. ¿Qué tipo de arquitectura sería la más adecuada?

## Decision Drivers

* Se destaca la modularidad y la capacidad de expansión por encima de los efectos negativos planteados
* Posibilidad de integración de un módulo Clientes que gestione el acceso a los datos personales de los usuarios
* Posibilidad de integración de un módulo Pedidos que gestione las peticiones de pedidos
* Posibilidad de integración de un módulo Reparto que gestione el número de camiones en cada zona
* Posibilidad de integración de un módulo Rutas que determine y comuinique la mejor ruta a seguir a cada uno de los camiones de la empresa
* Posibilidad de un módulo Estadísticas que envíe información sobre el estado de los pedidos a los clientes (información de envío, parámetros en tiempo real de los camiones de reparto e información acerca de sugerencias y recomendaciones a clientes)
* Posibilidad de integración de un módulo Incidencias que transmita incidencias sobre el reparto (camión averiado, pedido no entregado o reparto cancelado, entre otras) a los gestores de rutas que lo necesiten
* Posibilidad de integración de un módulo Pagos externo, que funciona como pasarela de pago y que garantiza su seguridad y fiabilidad
* Posibilidad de integración de un módulo central GestorPedidos, que funcione como medio de comunicación y mediación con otros módulos, concretamente los módulos Clientes, Pedidos, Reparto e Incidencias mencionados anteriormente

## Considered Options

* Arquitectura basada en microservicios
* Arquitectura por niveles (3 niveles)
* Arquitectura orientada a servicios
* Arquitectura orientada a eventos

## Decision Outcome

Chosen option: "Arquitectura basada en microservicios", because se adapta mejor a las necesidades del sistema necesitado.

### Positive Consequences

* Mayor escalabilidad del sistema
* Menor grado de acoplamiento
* Mayor fiabilidad ante posibles fallos
* Posibilidad de una única IU

### Negative Consequences

* Mayor congestión y latencia del sistema
* Riesgo de integridad de los datos
* Mayor riesgo de caída del sistema
* Mayor cantidad de recursos utilizados
