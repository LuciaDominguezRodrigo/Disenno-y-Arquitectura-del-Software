# Necesidad de comunicación rápida entre microservicios

* Status: accepted
* Deciders: 2
* Date: 2023-10-20

Technical Story: RF-6, RF-7

## Context and Problem Statement

Puesto que se gestionan datos en tiempo real dentro de la aplicación, el sistema debe de responder lo antes posible, ¿qué sistema es el más adecuado para la comunicación entre microservicios?

## Decision Drivers

* Es posible unificar la comunicación entre 2 microservicios y entre un microservicio y la API

## Considered Options

* HTTP/REST
* gRPC
* WebSockets

## Decision Outcome

Chosen option: "gRPC", because proporciona una comunicación mucho más rápida entre microservicios, necesarias para el envío y recepción de datos en tiempo real

### Positive Consequences

* Mayor rapidez en la comunicación al ser compatible con streaming de datos
* Interoperabilidad al ser independiente del lenguaje de programación utilizado

### Negative Consequences

* Consumo de muchos recursos del sistema
* Complejidad del protocolo
