# Necesidad de comunicación rápida entre microservicios

* Status: accepted
* Deciders: 2
* Date: 2023-10-20

Technical Story: RF-6, RF-7

## Context and Problem Statement

Puesto que se gestionan datos en tiempo real dentro de la aplicación, el sistema debe de responder lo antes posible, ¿qué sistema es el más adecuado para la comunicación entre microservicios?

## Decision Drivers

* Puntos positivos relevantes de lado de ambas alternativas
* Posibilidad de adaptación de la comunicación entre ambos protocolos

## Considered Options

* HTTP/REST
* gRPC
* WebSockets
* Protocolo mixto, usando gRPC en comunicaciones entre microservicios que requieran menor latencia y mayor velocidad de comunicación (es decir, las involucradas con el módulo GestorPedidos) y HTTP/REST en el resto de comunicaciones

## Decision Outcome

Chosen option: "Protocolo mixto, usando gRPC en comunicaciones entre microservicios que requieran menor latencia y mayor velocidad de comunicación (es decir, las involucradas con el módulo GestorPedidos) y HTTP/REST en el resto de comunicaciones", because proporciona una comunicación mucho más rápida entre microservicios, necesarias para el envío y recepción de datos en tiempo real, sin perder la sencillez, los estándares de seguridad y la comunicación asíncrona

### Positive Consequences

* Posibilidad de transmisión de datos en streaming mediante gRPC
* Comunicación asíncrona mediante HTTP/REST
* Sistema más sencillo de mantener y operar

### Negative Consequences

* Falta de unificación de protocolos
* Falta de interoperabilidad nativa entre ambos protocolos
