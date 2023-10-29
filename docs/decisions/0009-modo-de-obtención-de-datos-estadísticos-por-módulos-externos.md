# Modo de obtención de datos estadísticos por módulos externos

* Status: accepted
* Deciders: 2
* Date: 2023-10-28

Technical Story: RF-7, RF-8

## Context and Problem Statement

El componente Estadísticas de la arquitectura recoge datos de diversas fuentes y genera resultados estadísticos útles para otros módulos, pero ¿Cómo reciben o recogen esos módulos los datos?

## Decision Drivers

* Mejor un flujo de peticiones estrictamente necesarias a un flujo constante de datos no necesarios en todo momento

## Considered Options

* A través del módulo Estadísticas mediante una API propia, mediante peticiones
* Mediante la recogida de los datos relevantes para los módulos
* A través del módulo Estasdísticas mediante la combinación de una API propia y WebSockets

## Decision Outcome

Chosen option: "A través del módulo Estasdísticas mediante la combinación de una API propia y WebSockets", because comes out best.

### Positive Consequences

* Más modularidad
* Más eficiencia (los datos se pasan cuando sea necesario, no siempre)

### Negative Consequences

* Necesidad de hacer peticiones constantemente
* Las conexiones se mantienen abiertas
