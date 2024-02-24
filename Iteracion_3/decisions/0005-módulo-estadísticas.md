# Módulo estadísticas

* Status: proposed
* Date: 2024-02-20

## Context and Problem Statement

El módulo estadísticas proporciona información sobre el estado de los pedidos, la situación en tiempo real de los camiones e información de los clientes.

## Decision Drivers

* RF3.4 Módulo Estadísticas

## Considered Options

* Una clase Estadística que acceda a los 3 tipos de estadísticas
* Una clase Estadística, una clase por cada tipo de estadística y uso del patrón Strategy

## Decision Outcome

Chosen option: 
"Una clase Estadística, una clase por cada tipo de estadística y uso del patrón Strategy", because cumple con los requisitos pedidos del sistema de tener distintos tipos de estadísticas, mejora la escalabilidad y promueve la encapsulación. El uso del patrón Strategy mejora la calidad del diseño y facilita la elección del tipo de estadística deseada.

## Pros and Cons of the Options
### Una clase Estadística que acceda a los 3 tipos de estadísticas
Una única clase Estadística desde la que se pueda consultar los distintos tipo de estadísticas posibles (info clientes, estado pedidos, tiempo real camiones).

* Bad, because no hay división entre los distintos tipos de estadísticas que se pueden solicitar.
* Bad, because alto acoplamiento y disminuye la escalabilidad.

### Una clase Estadística y una clase por cada tipo de estadística y uso del patrón Strategy
Una clase Estadística, otra Estadísticas Pedidos, Estadísticas info clientes y Estadísticas estado camiones que se seleccionan según el tipo de estadística solicitada por medio del patrón Strategy.

* Good, because promueve la separación de responsabilidades específicas de cada tipo de estadística.
* Good, because mejora escalabilidad.
* Good, because el patrón Strategy cumple el Principio de abierto/cerrado.
* Bad, because el uso del patrón puede aumentar la complejidad del sistema.
