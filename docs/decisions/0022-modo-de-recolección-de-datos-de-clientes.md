# Modo de recolección de datos de clientes

* Status: proposed
* Date: 2023-11-02

Technical Story: RF-4

## Context and Problem Statement

Se necesita tener los datos actualizados de todos los clientes dados de alta en el sistema en todo momento

## Decision Drivers

* Necesidad de frecuente actualización para garantización de ultimidad de los datos
* Posibilidad de edición de los datos para su corrección

## Considered Options

* Peticiones periódicas de obtención de los datos de los clientes a la Base de datos
* Peticiones ocasionales en situaciones de necesidad de obtención de los datos de los clientes a la Base de datos

## Decision Outcome

Chosen option: "Peticiones ocasionales en situaciones de necesidad de obtención de los datos de los clientes a la Base de datos", because comes out best.

### Positive Consequences

* Menor latencia con menos peticiones
* Seguridad de veridicidad de los datos
* Fácil acceso y adición/modificación

### Negative Consequences

* Posibles pérdidas de datos
* Ineficaz organización y filtración de los datos
