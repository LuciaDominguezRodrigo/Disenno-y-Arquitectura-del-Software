# Modo de alojamiento de los microservicios

* Status: accepted
* Deciders: Blas, Marcos
* Date: 2023-10-31

Technical Story: RF-1, RF-1.2

## Context and Problem Statement

Se quiere decidir el soporte/soportes físicos donde se alojarán los distintos microservicios, de tal manera que cumpla con la fácil ampliación y modularidad

## Decision Drivers

* Proporcionar mayor posibilidad de escalabilidad
* Aclarar el diseño de la organización de la lógica de negocio
* Mejorar la estabilidad del sistema
* Mejorar la organización y jerarquización de los microservicios

## Considered Options

* Alojar todos los microservicios en un único servidor
* Alojar cada microservicio en un servidor
* Alojar en un único servidor los microservicios que utilizan el módulo GestorPedidos, y en otro servidor los restantes

## Decision Outcome

Chosen option: "Alojar en un único servidor los microservicios que utilizan el módulo GestorPedidos, y en otro servidor los restantes", because comes out best.

### Positive Consequences

* No habría necesidad de modificar las APIs
* Separación de responsabilidades
* Buen equilibrio organización-estabilidad
* Separación de servicios del cliente/internos
* Mayor fiabilidad frente a caídas

### Negative Consequences

* Mayor gasto económico
* Ligero incremento de latencia
* Mayor complejidad en la organización
