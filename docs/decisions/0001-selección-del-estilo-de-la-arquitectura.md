# Selección del estilo de la arquitectura

* Status: accepted
* Deciders: 2
* Date: 2023-10-19

Technical Story: RF-1, RF-1.2

## Context and Problem Statement

Se requiere un sistema con aruitectura orientada a microservicios, que sea flexible, modular y fácilmente expandible. ¿Qué tipo de arquitectura sería la más adecuada?

## Decision Drivers

* Se destaca la modularidad y la capacidad de expansión por encima de los efectos negativos planteados

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
