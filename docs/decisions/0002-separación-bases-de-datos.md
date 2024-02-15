# Separación bases de datos

* Status: proposed
* Date: 2024-02-14

## Context and Problem Statement

El sistema debe contar con dos bases de datos distintas para almacenar en la capa de datos los datos de los clientes y de los pedidos por separado.

## Decision Drivers

* RF2. Información clientes y pedidos

## Considered Options

* Crear Base de datos Clientes y Base de datos Pedidos
* Crear BBDD única del sistema.

## Decision Outcome

Chosen option: "Crear Base de datos Clientes y Base de datos Pedidos", because garantiza una mayor seguridad de los datos y evita que el sistema colapse debido a un exceso de datos.

## Pros and Cons of the Options

### Crear Base de datos Clientes y Base de datos Pedidos

Se crean dos bases de datos diferentes que almacenan distintos tipos de datos según si es información de un cliente o de un pedido.

* Good, because Descentraliza las bases de datos.
* Good, because Mejor productividad.
* Good, because Mayor seguridad en caso de pérdida de alguna de ellas.
* Bad, because Posibles errores de conexion.
* Bad, because Requiere mantenimiento de dos bases de datos.

### Crear BBDD única del sistema.

Crear una única base de datos que guarde toda la información necesaria.

* Good, because Información centralizada.
* Good, because Mantenimiento de una única base de datos.
* Bad, because Menor seguridad en caso de pérdida de los datos.
* Bad, because Mantenimiento complejo.
