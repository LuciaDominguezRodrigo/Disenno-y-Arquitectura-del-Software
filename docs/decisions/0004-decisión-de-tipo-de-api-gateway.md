# Decisión de tipo de API Gateway

* Status: accepted
* Deciders: 1
* Date: 2023-10-19

Technical Story: RF-10

## Context and Problem Statement

De entre todas las tecnologías de API Gateway disponibles, es necesario elegir una de ellas para la implementación del sistema. ¿Qué alternativa elegir?

## Considered Options

* Kong
* Nginx
* Apigee

## Decision Outcome

Chosen option: "Kong"

### Positive Consequences

* Buena respuesta ante alta demanda de tráfico
* Altamente escalable por gran cantidad de librerías
* Adecuado para incorporación de contenedores de microservicios
* Seguridad mediante certificados SSL

### Negative Consequences

* Complejidad en configuración
* Curva de aprendizaje lenta
