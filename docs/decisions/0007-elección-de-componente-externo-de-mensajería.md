# Elección de componente externo de mensajería

* Status: accepted
* Deciders: 1
* Date: 2023-10-20

Technical Story: RF-8, RF-11

## Context and Problem Statement

Es necesario un sistema capaz de notificar las incidencias, las rutas a seguir por los camiones y la información sobre un pedido realizado por un cliente. ¿Qué sistema sería capaz de gestionar los mensajes de forma fiable?

## Considered Options

* AMQP, MQTT, STOMP (Sistema publicación-suscripción)
* Apache Kafka
* WNS, Google GCM, AWS SNS (servicio de notificación)
* RabbitMQ

## Decision Outcome

Chosen option: "RabbitMQ", because opción más conveniente que las demás

### Positive Consequences

* Posibilidad de priorizar mensajes
* Presencia de librerías estándar

### Negative Consequences

* Menor rendimiento
* Menor abstracción
