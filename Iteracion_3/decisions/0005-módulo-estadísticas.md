# Módulo estadísticas

* Status: proposed
* Date: 2024-02-20

## Context and Problem Statement

El módulo estadísticas proporciona información sobre el estado de los pedidos, la situación en tiempo real de los camiones e información de los clientes.

## Decision Drivers

* RF3.4 Módulo Estadísticas

## Considered Options

* Módulo Estadísticas
* Patrón Strategy

## Decision Outcome

Chosen options: 
"Módulo Estadísticas", because cumple con los requisitos pedidos del sistema
"Patrón Strategy", because mejora la calidad del diseño y facilita la elección del tipo de estadística deseada.

## Pros and Cons of the Options
### Patrón Strategy
Emplear el patrón Strategy para seleccionar el tipo de estadística que se desea consultar.

* Good, because Cumple el Principio de abierto/cerrado.
* Good, because Permite aislar los detalles de implementación.
* Bad, because Aumenta la complejidad del sistema.


### Módulo Estadísticas

A través del módulo estadísticas se permite acceder al estado de los pedidos, la ubicación de los camiones en tiempo real y la información de los clientes.
