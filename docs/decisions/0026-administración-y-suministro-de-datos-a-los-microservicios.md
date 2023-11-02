# Administración y suministro de datos a los microservicios

* Status: proposed
* Date: 2023-11-02

Technical Story: RF-3

## Context and Problem Statement

Dada la complicación que supondría dar acceso libre a las BBDD a todos los microservicios, se requiere un componente que suministre los datos relevantes a cada microservicio. ¿Cuál sería la mejor alternativa?

## Decision Drivers

* Simplificación del proceso de obtención de daos

## Considered Options

* Utilización de un patrón Proxy
* Componente administrador de peticiones SQL con patrón Facade

## Decision Outcome

Chosen option: "Componente administrador de peticiones SQL con patrón Facade", because comes out best.

### Positive Consequences

* Menos complejidad en el acceso a las BBDD
* Más seguridad de los datos
* Control sobre cambios en los datos

### Negative Consequences

* Menor modularidad
* Mayor nivel de dependencia entre clases

## Pros and Cons of the Options

### Utilización de un patrón Proxy

Controla el acceso al objeto original, permitiendo hacer algo antes o después de que la solicitud llegue al mismo.

* Good, because Funcionamiento continuo aun fallando los microservicios
* Good, because Mayor control sobre los datos que se proporcionan
* Bad, because Peor respuesta ante peticiones

### Componente administrador de peticiones SQL con patrón Facade

Se añade un componente que haga de intermediario entre los microservicios y las BBDD, proporcionandole unicamente los datos que necesitan

* Good, because Aislamiento de la complejidad de las BBDD
* Bad, because Respuestas más lentas ante peticiones
