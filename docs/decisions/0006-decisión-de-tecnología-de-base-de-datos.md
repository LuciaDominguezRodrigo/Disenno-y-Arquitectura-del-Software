# Decisión de tecnología de Base de Datos

* Status: accepted
* Deciders: 1
* Date: 2023-10-19

Technical Story: RF-3

## Context and Problem Statement

Para acceder y hacer peticiones a una Base de Datos es necesario definir el tipo de tecnología que implementa. ¿Cuál se debe usar?

## Considered Options

* SQL
* NoSQL

## Decision Outcome

Chosen option: "SQL", because es más adecuada para el tipo de arquitectura elegida.

### Positive Consequences

* Atomicidad
* Portabilidad

### Negative Consequences

* Posibles cambios en la estructura de la BD
