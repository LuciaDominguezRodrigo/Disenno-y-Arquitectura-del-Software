# Conexión con pasarela de pago de terceros

* Status: accepted
* Deciders: Blas, Marcos
* Date: 2023-10-31

Technical Story: RF-9

## Context and Problem Statement

Se requiere decidir una plataforma de terceros que permita realizar pagos de terceros que maneje de forma segura los datos bancarios de un cliente

## Decision Drivers

* Posibilidad de proteger la seguridad de las cuentas frente a accesos no autorizados en caso de brechas de seguridad
* Incrementar la seguridad del inicio de sesión
* Evitar abusos de creación de múltiples cuentas

## Considered Options

* Componente realización de terceros Redsys
* Componente realización de terceros Niubiz
* Componente realización de terceros 2checkout
* Componente realización de cargos personalizado

## Decision Outcome

Chosen option: "Componente realización de terceros Redsys", because comes out best.

### Positive Consequences

* Posibilidad de libre elección del método para el usuario
* Método alternativo en caso de fallo
* Mayor seguridad

### Negative Consequences

* Mayor tiempo de inicio de sesión
* Mayor complejidad para recuperar una cuenta
* El 2FA por SMS no es el más seguro
