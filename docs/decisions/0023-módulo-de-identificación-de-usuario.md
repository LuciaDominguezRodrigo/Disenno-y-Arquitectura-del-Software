# Módulo de identificación de usuario

* Status: accepted
* Deciders: Blas, Marcos
* Date: 2023-11-02

Technical Story: RF-5

## Context and Problem Statement

Se necesita permitir a un cliente el acceso a un componente controlado de pedidos donde poder realizar y gestionarlos

## Decision Drivers

* Necesidad de conexión con módulo de estadísticas para obtener información
* Posibilidad de implementación de un patrón Factory con una clase validadora que identifique al usuario mediante su contraseña y su teléfono móvil
* Posibilidad de implementación de un patrón Cadena de Responsabilidad que deje acceder al usuario al sistema dependiendo de los permisos que tenga concedidos.
* Permite la limitación de pedidos de ese usuario a un número determinado de intentos
* Posibilidad de proteger la seguridad de las cuentas frente a accesos no autorizados en caso de brechas de seguridad
* Permite la seguridad del inicio de sesión

## Considered Options

* Acceso por credenciales (contaseña)
* Acceso por auteticación (teléfono móvil)
* Acceso por credenciales mediante contraseña y posterior verificación mediante teléfono móvil 

## Decision Outcome

Chosen option: "Acceso por credenciales y posterior verificación y autenticación para la identificación que permita la limitación de pedidos", because comes out best.

### Positive Consequences

* Proporción al cliente de información en todo momento en tiempo real
* Fácil realización de pedidos sin necesidad de intervención interna o de terceros
* Mayor seguridad y efectividad

### Negative Consequences

* Alta dependencia del correcto funcionamiento del sistema
* Mayor tiempo de inicio de sesión
* Mayor complejidad para recuperar una cuenta

