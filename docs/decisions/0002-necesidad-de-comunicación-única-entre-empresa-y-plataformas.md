# Necesidad de comunicación única entre empresa y plataformas

* Status: accepted
* Deciders: 2
* Date: 2023-10-19

Technical Story: RF-1.1

## Context and Problem Statement

Es necesario un sistema de envío/recepción de paquetes unificado que permita la comunicación bidireccional en diferentes tipos de dispositivos. ¿Cuál es el mejor protocolo en este caso?

## Decision Drivers

* Se requiere un protocolo capaz de comunicarse con los usuarios a través de un navegador web o aplicación conectada. En este caso, gRPC no posee compatibilidad completa al basarse en la tecnología HTTP/2.

## Considered Options

* Protocolo HTTP/REST
* gRPC
* GraphQL

## Decision Outcome

Chosen option: "Protocolo HTTP/REST", because se logra una compatibilidad completa y una unificación de protocolo para todos los dispositivos con un navegador

### Positive Consequences

* Protocolo único para diferentes dispositivos
* Campatibilidad completa en navegadores

### Negative Consequences

* Menor rendimiento
* Pérdida de envío de datos en stream
