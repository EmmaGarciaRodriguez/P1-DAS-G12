# Módulo repartos y rutas y Selección de algoritmo

* Status: proposed
* Date: 2024-02-15

## Context and Problem Statement

El módulo Repartos y rutas debe gestionar el reparto y las rutas de los paquetes. Además, el sistema cuenta con dos algoritmos de optimización que se seleccionan en función de la demora del camión.

## Decision Drivers

* RF3.3 Módulo Repartos y rutas

## Considered Options

* Una única clase que gestione Reparto y Rutas y uso del patrón Strategy
* Dos clases separadas Reparto y Rutas y uso del patrón Strategy

## Decision Outcome

Chosen option: "Una única clase que gestione Reparto y Rutas y uso del patrón Strategy", because el uso de una única clase que englobe todas las funciones relacionadas con las rutas y los repartos de los paquetes, aumenta la modularidad. Además, el uso del patrón Strategy mejora la calidad del diseño y facilita la elección del algoritmo más óptimo.

## Pros and Cons of the Options

### Una única clase que gestione Reparto y Rutas y uso del patrón Strategy

El módulo Repartos y rutas permite gestionar el reparto de las flotas de transporte a los clientes. Además, se emplea el patrón Strategy para seleccionar el algoritmo de optimización que se va a emplear en funcion de la demora del camión.

* Good, because el patrón Strategy permite aislar los detalles de implementación.
* Good, because el módulo Gestión Repartos y Rutas de la lógica de negocio englobará todas las funciones relacionadas con los repartos y las rutas, aumentando la modularidad y escalabilidad.
* Good, because el patrón Strategy cumple el Principio de abierto/cerrado.
* Bad, because el uso del patrón puede aumentar la complejidad del sistema.


###  Dos clases separadas Reparto y Rutas y uso del patrón Strategy

El módulo Repartos y rutas cuenta con dos clases separadas "Repartos" y "Rutas" que se relacionan y permite gestionar el reparto de los paquetes a los clientes. Además, se emplea el patrón Strategy para seleccionar el algoritmo de optimización que se va a emplear en funcion de la demora del camión.

* Good, because el patrón Strategy permite aislar los detalles de implementación.
* Bad, because es necesaria una comunicación entre las clases "Reparto" y "Rutas" que complica el sistema y que podría solventarse si solo hubiera una clase que se encargara de la gestión de los repartos y las rutas simultáneamente.
* Good, because el patrón Strategy cumple el Principio de abierto/cerrado.
* Bad, because el uso del patrón puede aumentar la complejidad del sistema.
