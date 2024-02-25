# Rediseño Módulos Clientes y Pedidos

* Status: proposed
* Date: 2024-02-24

## Context and Problem Statement

La lógica de negocio debe contar con los módulos clientes, pedidos, repartos y rutas, y estadísticas.
- El módulo clientes permite a acceder los datos de personales de los clientes (identificador, nombre, apellidos, email y teléfono móvil).
- El módulo pedidos permite a los clientes realizar pedidos de productos.
- El módulo Reparto y rutas gestiona el reparto de los pedidos a los clientes y las rutas de los camiones. El sistema debe contar con un componente Incidencias que se encarga de reportar las incidencias durante el reparto (camión averiado, demora o no entrega de pedido).
- El módulo Estadísticas proporciona información sobre los clientes, sobre el estado de los pedidos y la situación en tiempo real de los camiones.

## Decision Drivers

* RF3. Lógica de negocio
* RF3.1 Módulo Clientes
* RF3.2 Módulo Pedidos

## Considered Options

* Crear los módulos Cliente, Estadísticas, Repartos y Rutas
* Crear los módulos Cliente, Pedidos, Estadísticas, Repartos y Rutas

## Decision Outcome

Chosen option: "Crear los módulos Cliente, Estadísticas, Repartos y Rutas", because permite cumplir con la arquitectura microservicios y omite módulos innecesarios.


### Crear los módulos Cliente, Estadísticas, Repartos y Rutas

Se crean los módulos Clientes, Pedidos, Repartos y rutas, y Estadísticas que requiere el sistema para realizar las funciones principales. Dichos módulos se encuentran en la capa de lógica de negocio.
El módulo Cliente permite a los clientes consultar sus datos personales: identificador, nombre, apellidos, email o teléfono móvil. Además, desde el módulo Cliente, el cliente puede realizar una compra.


### Crear los módulos Cliente, Pedidos, Estadísticas, Repartos y Rutas

Se crean los módulos Clientes, Pedidos, Repartos y rutas, y Estadísticas que requiere el sistema para realizar las funciones principales. Dichos módulos se encuentran en la capa de lógica de negocio.
El módulo Cliente permite a los clientes consultar sus datos personales: identificador, nombre, apellidos, email o teléfono móvil.
Por último, desde el módulo Pedidos el cliente podrá realizar una compra.

