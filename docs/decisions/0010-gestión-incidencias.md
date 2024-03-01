# Gestión Incidencias

* Status: proposed
* Date: 2024-02-28

## Context and Problem Statement

Se deben reportar las incidencias que tienen lugar durante el reparto de los pedidos. Estas incidencias puedes ser de 3 tipos: camión averiado, demora, pedido no entregado.

## Decision Drivers

* RF3.3.1 Incidencias

## Considered Options

* Un módulo Incidencias y uso del patrón Publish Subscribe
* La clase Gestor Repartos y Rutas se ocupa de reportar las incidencias

## Decision Outcome

Chosen option: "La clase Gestor Repartos y Rutas se ocupa de reportar las incidencias", no complica la lógica de negocio innecesariamente y es suficiente para solucionar dicho problema de diseño.

## Pros and Cons of the Options

### Un módulo Incidencias y uso del patrón Publish Subscribe

El sistema cuenta con un nuevo módulo de Incidencias que se relaciona con el módulo de Repartos y Rutas, y emplea el patrón Publish Subscribe que notifica los cambios en los estado de los repartos.

* Good, because Mejora la escalabilidad del sistema
* Good, because Permite que el sistema sea ampliado sin tener que modificar la arquitectura
* Bad, because Diseño más engorroso y aumenta la complejidad del sistema innecesariamente

### La clase Gestor Repartos y Rutas se ocupa de reportar las incidencias

El módulo reparto y rutas cuenta con una clase Gestor Repartos y rutas que se ocupará de reportar los tres tipos de incidencias que pueden darse

* Good, because simplifica la lógica de las incidencias y no añade complejidad innecesaria al sistema.
* Bad, because Complica introducir más tipos de incidencias.
