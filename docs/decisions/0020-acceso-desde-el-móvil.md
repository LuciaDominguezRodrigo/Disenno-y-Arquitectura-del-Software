# Acceso desde el móvil

* Status: rejected
* Date: 2023-10-31

Technical Story: RF-1.1

## Context and Problem Statement

Se quiere decidir el método de acceso al sistema desde dispositivos móviles

## Decision Drivers

* Aclarar el diseño de la arquitectura de la aplicación en el lado clilente
* Determinar el número de APIs a usar

## Considered Options

* Navegador integrado en aplicación móvil
* Aplicación móvil dedicada

## Decision Outcome

Chosen option: "Aplicación móvil dedicada", because comes out best.

### Positive Consequences

* No habría necesidad de cambiar las APIs
* Mejor experiencia de usuario en móvil
* Mayor velocidad
* Separación de acceso con respecto a los usuarios de navegador

### Negative Consequences

* Gran coste en tiempo de programación
* Organización ligeramente más compleja
