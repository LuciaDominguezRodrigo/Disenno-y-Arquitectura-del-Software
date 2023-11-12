# Localización de algoritmos de optimización de rutas y flotas de camiones

* Status: accepted
* Deciders: 2
* Date: 2023-10-28

Technical Story: RF-6

## Context and Problem Statement

Se requiere un módulo de algoritmos que tome decisiones acerca del posicionamiento y la ruta de cada uno de los camiones de la flota. ¿Dónde debería situarse este módulo?

## Decision Drivers

* Al requerir varios módulos de los resultados de los algoritmos, se prefiere separarlos de los microservicios para evitar dependencias

## Considered Options

* Modulo Reparto
* Modulo Rutas
* Modulo independiente dentro de la lógica de negocio

## Decision Outcome

Chosen option: "Modulo independiente dentro de la lógica de negocio", because comes out best.

### Positive Consequences

* Funcionamiento no ligado a otros microservicios
* Comunicación más directa de los datos

### Negative Consequences

* Presencia de componente software adicional
* Presencia de conexiones adicionales
