# Módulo de identificación de usuario

* Status: proposed
* Date: 2023-11-02

Technical Story: RF-5

## Context and Problem Statement

Se necesita permitir a un cliente el acceso a un componente controlado de pedidos donde poder realizar y gestionarlos

## Decision Drivers

* Posibilidad de controlar los pedidos por usuario por medio de autenticación
* Necesidad de conexión con módulo de estadísticas para obtener información

## Considered Options

* Acceso por credenciales
* Acceso por autencitación
* Acceso por credenciales y posterior verificación y autenticación para la identificación que permita la limitación de pedidos

## Decision Outcome

Chosen option: "Acceso por credenciales y posterior verificación y autenticación para la identificación que permita la limitación de pedidos", because comes out best.

### Positive Consequences

* Proporción al cliente de información en todo momento en tiempo real
* Fácil realización de pedidos sin necesidad de intervención interna o de terceros
* Mayor seguridad y efectividad

### Negative Consequences

* Alta dependencia del correcto funcionamiento del sistema
* Posibles caídas del sistema ante frecuentes peticiones
