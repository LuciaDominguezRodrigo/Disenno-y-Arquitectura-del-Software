# Elección de tipo de algoritmos de optimización

* Status: accepted
* Deciders: 2
* Date: 2023-10-28

Technical Story: RF-6, RF-7

## Context and Problem Statement

Se requieren 2 algoritmos de optimización de rutas y flotas de camiones. ¿Qué par de algorimos sería el más adecuado?

## Decision Drivers

* Se prefiere un algoritmo capaz de adaptarse a situaciones cambiantes

## Considered Options

* Enrutamiento en tiempo real y Redireccionamiento Dinámico
* Enrutamiento en tiempo real y Enrutamiento programado

## Decision Outcome

Chosen option: "Enrutamiento en tiempo real y Redireccionamiento Dinámico", because comes out best.

### Positive Consequences

* Mejor respuesta ante averías de camiones
* Menor planificación y dependencia
* Capacidad de detección y solución de averías

### Negative Consequences

* Menos predictibilidad de rutas
