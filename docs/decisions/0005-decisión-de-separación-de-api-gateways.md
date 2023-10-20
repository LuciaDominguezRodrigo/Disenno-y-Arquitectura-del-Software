# Decisión de separación de API Gateways

* Status: accepted
* Deciders: 1
* Date: 2023-10-19

Technical Story: RF-10

## Context and Problem Statement

Si las aplicaciones móviles y web requieren respuestas ligeramente diferentes (como el formato de datos o la adaptación de la interfaz de usuario), deben de tenerse o bien 2 APIs diferentes para tratar los datos de forma distinta, o bien usar patrones de adaptación de datos. ¿Qué elegir?

## Decision Drivers

* Es innecesario duplicar componentes software cuando los datos son muy similares

## Considered Options

* Duplicación de API Gateways (una para app movil y otra para app web)
* Utilización de patrones de adaptación de datos

## Decision Outcome

Chosen option: "Utilización de patrones de adaptación de datos", because es más eficiente y correcto

### Positive Consequences

* Evitar redundancia de componentes
* Evitar redundancias de datos

### Negative Consequences

* Necesidad de transformar los datos de una vista a otra
