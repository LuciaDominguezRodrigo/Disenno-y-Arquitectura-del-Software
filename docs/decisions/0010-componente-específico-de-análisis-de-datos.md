# Componente específico de análisis de datos

* Status: accepted
* Deciders: 2
* Date: 2023-10-28

Technical Story: RF-7

## Context and Problem Statement

Dentro del módulo Estadísticas se requiere un componente que analice y calcule los valores necesarios. ¿Cómo se distribuiría el trabajo?

## Decision Drivers

* Se considera más importante la velocidad de cálculo y la seguridad antes que la repetición de componentes con funcionamiento similar
* Posibilidad de incluir un módulo de tendencias temporales para identificar patrones estacionales, picos de actividad y cambios en el comportamiento de los datos en tiempo real
* Posibilidad de incluir un módulo de detección de anomalías para identificar desviaciones inusuales o valores atípicos en los datos en tiempo real, o problemas o eventos inesperados
* Posibilidad de incluir un módulo de estadísticas descriptivas para calcular valores básicos (promedio, mediana, desviación estándar, mínimo, máximo, etc.)
* Posibilidad de incluir un módulo de análisis de correlación para identificar relaciones entre diferentes variables dentro de los datos y así comprender cómo se relacionan entre sí
* Posibilidad de incluir un módulo de clasificación de datos para categorizar los datos en tiempo real en diferentes grupos o segmentos
* Posibilidad de incluir un módulo de predicciones para realizar predicciones sobre cómo evolucionarán los datos en el futuro
* Posibilidad de incluir un módulo de visualización en tiempo real para mostrar a los usuarios en tiempo real y resultados de análisis
* Posibilidad de incluir un módulo de segmentación de audiencia para dividir la audiencia en grupos con características similares (útil para personalizar contenido y ofertas)
* Posibilidad de incluir un módulo de monitoreo de rendimiento para medir el rendimiento y la salud de determinados microservicios en tiempo real
* Posibilidad de incluir un módulo de filtrado y preprocesamiento, que filtra y procesa datos para garantizar que solo se analicen datos relevantes y de calidad

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
