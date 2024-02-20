# Módulo repartos y rutas y selección de algoritmo

* Status: proposed
* Date: 2024-02-15

## Context and Problem Statement

El módulo Repartos y rutas debe gestionar el reparto y las rutas de los paquetes. Además, el sistema cuenta con dos algoritmos de optimización que se seleccionan en función de la demora del camión.

## Decision Drivers

* RF3.3 Módulo Repartos y rutas

## Considered Options

* Utilizar patrón Strategy
* Gestión del reparto

## Decision Outcome

Chosen option: "Utilizar patrón Strategy", because mejora la calidad del diseño y facilita la elección del algoritmo.

## Pros and Cons of the Options

### Utilizar patrón Strategy

Emplear el patrón Strategy para seleccionar el algoritmo de optimización que se va a emplear en funcion de la demora del camión.

* Good, because Cumple el Principio de abierto/cerrado.
* Good, because Permite aislar los detalles de implementación.
* Bad, because Aumenta la complejidad del sistema.

### Gestión del reparto

El módulo Repartos y rutas permite gestionar el reparto de las flotas de transporte a los clientes.
