# Necesidad de incremento en seguridad de datos en tiempo real

* Status: accepted
* Date: 2023-10-28

Technical Story: RF-2

## Context and Problem Statement

Para la toma de decisiones por parte de los algoritmos, es necesario el flujo de datos de carácter sensible tanto para los usuarios como para los camiones (datos personales, ubicación en tiempo real). ¿Cómo se podría incrementar el nivel de seguridad de los datos?

## Decision Drivers

* Se prefiere conservar gran parte de los protocolos de comunicación actual antes que la implementación de métodos de cifrado más avanzados

## Considered Options

* Incorporación del protocolo HTTPS a conexiones actuales
* Uso de TLS entre cliente y servidor
* Uso de SSH entre cliente y servidor

## Decision Outcome

Chosen option: "Incorporación del protocolo HTTPS a conexiones actuales", because comes out best.

### Positive Consequences

* Compatibilidad completa con API REST
* Más sencillo
* Menos costoso

### Negative Consequences

* Menor grado de seguridad
