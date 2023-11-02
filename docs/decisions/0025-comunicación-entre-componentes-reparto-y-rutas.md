# Comunicación entre componentes Reparto y Rutas

* Status: proposed
* Date: 2023-11-02

Technical Story: RF-11

## Context and Problem Statement

Ante la necesidad de separación de los módulos Reparto y Rutas debido a su gran complejidad, es necesario establecer su comunicación mediante el uso de patrones de diseño. ¿Cuál es el más adecuado?

## Decision Drivers

* Se considera más importante la comunicación directa entre componentes que la adaptación de datos entre los mismos

## Considered Options

* Patrón Adapter
* Patrón Bridge

## Decision Outcome

Chosen option: "Patrón Bridge", because comes out best.

### Positive Consequences

* Funcionamiento a alto nivel
* Sigue el principio de abierto/cerrado

### Negative Consequences

* Aumento de la complejidad del código

## Pros and Cons of the Options

### Patrón Adapter

Se apatan los datos de cada una de las clases a la otra, surgiendo así la comunicación

* Good, because Se mantiene el principio de responsabilidad única
* Bad, because Aumenta la complejidad

### Patrón Bridge

Dos modulos que tienen mucho que ver entre sí se dividen en jerarquías con posibilidad de desarrollo independiente

* Good, because Posibilidad de creación de componentes muy diferentes entre sí
* Bad, because Poca cohesión en modulos muy relacionados
