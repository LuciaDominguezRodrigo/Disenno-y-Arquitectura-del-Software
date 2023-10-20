# Elección de un adaptador entre comunicaciones gRPC y HTTP/REST

* Status: accepted
* Deciders: 1
* Date: 2023-10-20

## Context and Problem Statement

Al elegirse una comunicación mixta entre protocolos gRPC para comunicaciones rápidas y GTTP/REST para comunicaciones convencionales, es necesario que la comunicación se transmita si se deben de usar ambos protocolos en una misma comunicación. ¿Qué opción es la más adecuada?

## Decision Drivers

* Posibilidad de comunicar todos los servicios mediante el uso de pocos módulos software

## Considered Options

* Puente entre HTTP/REST y gRPC
* Adaptadores a HTTP/REST y gRPC
* Selección del protocolo en función del servicio

## Decision Outcome

Chosen option: "Adaptadores a HTTP/REST y gRPC", because se considera más importante, al haber muchos servicios de ambas clases, la no redundancia de componentes software en cada servicio

### Positive Consequences

* Separación del módulo de la lógica primaria de los servicios
* Posibilidad de reutilización
* Posibilidad de introducción de nuevos adaptadores en caso necesario

### Negative Consequences

* Disminuye la modularidad
