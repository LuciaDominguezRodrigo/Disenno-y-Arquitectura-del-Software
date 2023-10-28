# Orden de prioridad de sucesos para elección de algoritmo optimizador dependiendo de los datos

* Status: accepted
* Deciders: 2
* Date: 2023-10-28

Technical Story: RF-5, RF-6

## Context and Problem Statement

Se requiere de un componente que seleccione entre los 2 algoritmos dependiendo de las necesidades de las flotas de camiones y rutas, pero ¿qué factor debe ser determinante para el cambio de un algoritmo a otro?

## Decision Drivers

* Se prefiere remarcar como determinante la avería de un camión como suceso que determine el cambio de algoritmo

## Considered Options

* Avería de camión, tráfico pesado, condiciones meteorológicas adversas
* Avería de camión, condiciones meteorológicas adversas, tráfico pesado
* Condiciones meteorológicas adversas, avería de camión, tráfico pesado

## Decision Outcome

Chosen option: "Avería de camión, tráfico pesado, condiciones meteorológicas adversas", because comes out best.

### Positive Consequences

* Avería de camión como suceso más importante
* Suceso no evitable frente a sucesos evitables mediante selección de otras rutas

### Negative Consequences

* Menos control sobre las rutas
