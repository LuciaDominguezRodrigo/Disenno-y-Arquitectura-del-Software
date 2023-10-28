# Elección de algoritmos de optimización de posición geográfica de camiones

* Status: accepted
* Deciders: 2
* Date: 2023-10-28

Technical Story: RF-6, RF-7

## Context and Problem Statement

Es necesario un algoritmo que redireccione los camiones en caso de avería. ¿Cuál es el más adecuado?

## Decision Drivers

* Se prefiere la realización de cálculos con independencia del número de flotas de camiones en cada momento

## Considered Options

* K-Means
* DBSCAN

## Decision Outcome

Chosen option: "DBSCAN", because comes out best.

### Positive Consequences

* No necesita conocer el número de flotas inicial
* Capacidad para redirigir puntos lejanos
* Mayor velocidad de cálculo

### Negative Consequences

* Menos eficiente
* Más pesado y costoso
