# Módulo estadísticas

* Status: proposed
* Date: 2024-02-20

## Context and Problem Statement

El módulo estadísticas proporciona información sobre el estado de los pedidos, la situación en tiempo real de los camiones e información de los clientes.

## Decision Drivers

* RF3.4 Módulo Estadísticas

## Considered Options

* Una clase Estadística que guarde los 3 tipos de estadísticas
* Una clase Estadística, una clase por cada tipo de estadística y uso del patrón Strategy

## Decision Outcome

Chosen option: 
"Una clase Estadística, una clase por cada tipo de estadística y uso del patrón Strategy", because cumple con los requisitos pedidos del sistema de tener distintos tipos de estadísticas, mejora la escalabilidad y promueve la encapsulación. El uso del patrón Strategy mejora la calidad del diseño y facilita la elección del tipo de estadística deseada.

## Pros and Cons of the Options
### Una clase Estadística que guarde los 3 tipos de estadísticas
Una única clase Estadística desde la que se pueda consultar los distintos tipo de estadísticas posibles (info clientes, estado pedidos, tiempo real camiones).

* Good, because Cumple el Principio de abierto/cerrado.
* Good, because Permite aislar los detalles de implementación.
* Bad, because Aumenta la complejidad del sistema.


### Una clase Estadística y una clase por cada tipo de estadística y uso del patrón Strategy

* Good, because el patrón Strategy permite aislar los detalles de implementación.
* Good, because el módulo Gestión Repartos y Rutas de la lógica de negocio englobará todas las funciones relacionadas con los repartos y las rutas, aumentando la modularidad y escalabilidad.
* Good, because el patrón Strategy cumple el Principio de abierto/cerrado.
* Bad, because el uso del patrón puede aumentar la complejidad del sistema.
