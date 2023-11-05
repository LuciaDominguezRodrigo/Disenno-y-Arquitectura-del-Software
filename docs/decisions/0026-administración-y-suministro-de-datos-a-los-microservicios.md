# Administración y suministro de datos a los microservicios

* Status: accepted
* Deciders: Marcos, Blas
* Date: 2023-11-02

Technical Story: RF-3

## Context and Problem Statement

Dada la complicación que supondría dar acceso libre a las BBDD a todos los microservicios, se requiere un componente que suministre los datos relevantes a cada microservicio. ¿Cuál sería la mejor alternativa?

## Decision Drivers

* Simplificación del proceso de obtención de datos
* Necesidad de frecuente actualización para garantización de ultimidad de los datos
* Posibilidad de actualización de los datos para su corrección


## Considered Options

* Peticiones periódicas de obtención de los datos a la Base de datos mediante la utilización de un patrón Proxy
* Peticiones periódicas de obtención de los datos a la Base de datos mediante un componente administrador de peticiones SQL con patrón Facade
* Peticiones ocasionales en situaciones de necesidad de obtención de datos a la Base de datos mediante la utilización de un patrón Proxy
* Peticiones ocasionales en situaciones de necesidad de obtención de datos a la Base de datos mediante la utilización de un componente administrador de peticiones SQL con patrón Facade

## Decision Outcome

Chosen option: "Peticiones ocasionales en situaciones de necesidad de obtención de los datos de los clientes a la Base de datos mediante la utilización de un componente administrador de peticiones SQL con patrón Facade", because comes out best.

### Positive Consequences

* Más control sobre cambios en los datos
* Menor latencia con menos peticiones
* Seguridad de veridicidad de los datos
* Fácil acceso y edición/modificación

### Negative Consequences

* Menor modularidad
* Mayor nivel de dependencia entre clases
* Posibles pérdidas de datos
* Ineficaz organización y filtración de los datos

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
