# Componente específico de análisis de datos

* Status: accepted
* Date: 2023-10-28

Technical Story: RF-7, RF-8

## Context and Problem Statement

Dentro del módulo Estadísticas se requiere un componente que analice y calcule los valores necesarios. ¿Cómo se distribuiría el trabajo?

## Decision Drivers

* Se considera más importante la velocidad de cálculo y la seguridad antes que la repetición de componentes con funcionamiento similar

## Considered Options

* Presencia de módulo analizador de datos común para todo el componente Estadísticas
* Presencia de analizador de un tipo de datos específico para cada estadístico

## Decision Outcome

Chosen option: "Presencia de analizador de un tipo de datos específico para cada estadístico", because comes out best.

### Positive Consequences

* Menos tráfico de datos en un solo componente
* Más seguridad
* Menos cuello de botella
* Más eficiencia en análisis de datos

### Negative Consequences

* Duplicidad de módulos con funcionamiento similar
* Aumento de la complejidad del módulo
