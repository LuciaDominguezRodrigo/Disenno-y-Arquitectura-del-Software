# Autenticación 2FA

* Status: rejected
* Date: 2023-10-31

Technical Story: RF-4

## Context and Problem Statement

Se requiere de una autenticación de todos los usuarios por medio de 2FA para incrementar la seguridad de la información de los clientes.

## Decision Drivers

* Posibilidad de proteger la seguridad de las cuentas frente a accesos no autorizados en caso de brechas de seguridad
* Incrementar la seguridad del inicio de sesión
* Evitar abusos de creación de múltiples cuentas

## Considered Options

* Código único por medio de SMS
* Código único por medio de correo electrónico
* Enlace único por correo electrónico
* Código generado por aplicación de terceros
* Combinación de varios métodos

## Decision Outcome

Chosen option: "Combinación de varios métodos", because comes out best.

### Positive Consequences

* Posibilidad de libre elección del método para el usuario
* Método alternativo en caso de fallo
* Mayor seguridad

### Negative Consequences

* Mayor tiempo de inicio de sesión
* Mayor complejidad para recuperar una cuenta
* El 2FA por SMS no es el más seguro
