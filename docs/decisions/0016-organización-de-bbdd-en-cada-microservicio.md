# Organización de BBDD en cada microservicio

* Status: accepted
* Deciders: 2
* Date: 2023-10-28

Technical Story: RF-3, RF-12

## Context and Problem Statement

Se necesita definir una oorganización de BBDD que soporte el gran flujo de datos de los microservicios. ¿Qué organización sería la más adecuada?

## Decision Drivers

* Posibilidad de salvaguardar la información con más necesidad de persistencia en una BBDD más segura y con menos tráfico
* Posibilidad de utilización de patrón de acceso CQRS, que divide las solicitudes entre comandos y lecturas, accediendo a las BBDD únicamente con permisos de lectura o escritura
* Posibilidad de implementación de "pool" de conexiones que reutilice las conexiones ya abiertas con las BBDD
* Posibilidad de incorporación de espacio de memoria de rápido acceso dedicado al almacenamiento de las consultas más frecuentes, para agilizar y ahorrar las consultas a las BBDD

## Considered Options

* Incorporación de SGBD que rigan el funcionamiento de ambas BBDD presentes
* Dividir BBDD, teniendo una BBDD para cada microservicio
* Presencia de una BBDD centralizada que guarde los datos más persistentes y otras BBDD independientes en cada microservicio con la información con más necesidad de refresco.

## Decision Outcome

Chosen option: "Presencia de una BBDD centralizada que guarde los datos más persistentes y otras BBDD independientes en cada microservicio con la información con más necesidad de refresco", because comes out best.

### Positive Consequences

* Más seguridad de datos
* Menor riesgo de caída del sistema ante inutilización de BBDD
* Menor sobrecarga de peticiones de las BBDD

### Negative Consequences

* Redundancia temporal de datos
* Necesidad de sincronización de BBDD propias con BBDD central
