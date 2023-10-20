# Decisión de separación de API Gateways

* Status: accepted
* Deciders: 1
* Date: 2023-10-19

Technical Story: RF-10

## Context and Problem Statement

Si las aplicaciones móviles y web requieren respuestas ligeramente diferentes (como el formato de datos o la adaptación de la interfaz de usuario), deben de tenerse o bien 2 APIs diferentes para tratar los datos de forma distinta, o bien usar patrones de adaptación de datos. ¿Qué elegir?

## Decision Drivers

* Mejor capacidad de tratamiento de datos
* Menores brechas de seguridad en el sistema

## Considered Options

* Presencia de dos API Gateways (una para app movil y otra para app web) comunicadas mediante un patrón Backend for Frontend
* Utilización de patrones de adaptación de datos

## Decision Outcome

Chosen option: "Presencia de dos API Gateways (una para app movil y otra para app web) comunicadas mediante un patrón Backend for Frontend", because se considera importante la seguridad y la transferencia fiable de datos

### Positive Consequences

* Mayor resistencia frente a brechas de seguridad
* Mayor capacidad de manejo de datos

### Negative Consequences

* Posible redundancia de datos
