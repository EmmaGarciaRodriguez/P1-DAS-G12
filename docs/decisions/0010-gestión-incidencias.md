# Gestión Incidencias

* Status: proposed
* Date: 2024-02-28

## Context and Problem Statement

La clase Incidencias reporta las incidencias que tienen lugar durante el reparto de los pedidos. Estas incidencias puedes ser de 3 tipos: camión averiado, demora, pedido no entregado.

## Decision Drivers

* RF3.3.1 Incidencias

## Considered Options

* Un módulo Incidencias y uso del patrón Publish Subscribe
* Una clase Incidencias en el módulo de Repartos y Rutas

## Decision Outcome

Chosen option: "Un módulo Incidencias y uso del patrón Publish Subscribe", because favorece el desacoplamiento de los módulos y permite conocer las incidencias que tienen lugar de una forma más eficiente.

## Pros and Cons of the Options

### Un módulo Incidencias y uso del patrón Publish Subscribe

El sistema cuenta con un nuevo módulo de Incidencias que se relaciona con el módulo de Repartos y Rutas, y emplea el patrón Publish Subscribe que notifica los cambios en los estado de los repartos.

* Good, because Mejora la escalabilidad del sistema
* Good, because Permite que el sistema sea ampliado sin tener que modificar la arquitectura
* Good, because Diseño más claro y sencillo

### Una clase Incidencias en el módulo de Repartos y Rutas

El sistema cuenta con una clase Incidencias dentro del módulo de Repartos y Rutas que recibe la información de los estados de los pedidos y la notifica a las partes interesadas.

* Good, because Relación directa con el gestor de Repartos y Rutas
* Bad, because No favorece el desacoplamiento de los módulos
* Bad, because No permite expandir el sistema
* Bad, because Complicar introducir más tipos de incidencias
