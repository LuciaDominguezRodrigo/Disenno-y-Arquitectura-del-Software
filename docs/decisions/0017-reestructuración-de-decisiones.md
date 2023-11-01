# Reestructuración de decisiones

* Status: accepted
* Deciders: 2
* Date: 2023-11-01

## Context and Problem Statement

Tras comprobar que el sistema definido anteriormente presenta un nivel de especificación mayor al deseado, se procede a modificar las decisiones menos relevantes, anulando aquellas que se consideren no válidas. Una decisión se considerará inválida si se produce un conflicto con nuevas decisiones tomadas

## Decision Drivers

* Se modifica la decisión 1, dependiendo ahora solamente del requisito RF-1.2
* Se modifica la decisión 2, dependiendo ahora de los requisitos RF-1.1
* Se elimina la decisión 3, pues se exige un protocolo de comunicación HTTP/REST en todo el sistema
* Se modifica la decisión 6, dependiendo solamente del requisito RF-3.
* Se elimina la decisión 7, sustituyendo esta por otra decisión
* Se eliminan las decisiones 8 y 9, pues se exige un protocolo de comunicación HTTP/REST en todo el sistema
* Se modifica la decisión 10, dependiendo solamente del requisito RF-7.
* Se modifica la decisión 11, dependiendo solamente del requisito RF-6.
* Se eliminan las decisiones 12, 13, 14 y 15, pues especifican concretamente el funcionamiento de los algoritmos
* Se elimina la decisión 16, pues se requieren únicamente 2 BBDD en el sistema
* Se elimina la decisión 5, pues se ha encontrado innecesaria la separación de APIs para interfaces web y móvil

## Considered Options

* Todas las modificaciones se aplican al diseño

## Decision Outcome

Chosen option: "Todas las modificaciones se aplican al diseño", because comes out best.

### Positive Consequences

* Ninguna

### Negative Consequences

* Repercute a las decisiones anteriormente tomadas
