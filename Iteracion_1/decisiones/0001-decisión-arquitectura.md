# Decisión arquitectura

* Status: proposed
* Date: 2024-02-08

## Context and Problem Statement

Se propone la arquitectura que mejor se adapta al sistema pedido por el cliente.

## Decision Drivers

* RF1. Arquitectura Microservicios

## Considered Options

* 001-Arquitectura Cliente-Servidor
* 002-Arquitectura por Capas

## Decision Outcome

Chosen option: "001-Arquitectura Cliente-Servidor", because la Arquitectura Cliente-Servidor se adapta mejor a un sistema basado en microservicios donde el cliente interacciona con los módulos del servidor y en el cual se necesita una capa de datos donde almacenar la información de los clientes y sus pedidos.

## Pros and Cons of the Options

### 001-Arquitectura Cliente-Servidor

* Good, because - Control centralizado: el control central reside en el servidor.
* Good, because - Comunicación entre Cliente y servidor más eficiente.
* Good, because - Escalabilidad vertical.
* Bad, because - Escalabilidad limitada.
* Bad, because - Dependencia del servidor.

### 002-Arquitectura por Capas

* Good, because - Desacoplamiento por capas (los cambios en una no afectan a otra).
* Good, because - Reutilización de componentes (modularidad y capas con funciones específicas).
* Good, because - Mejora la adaptabilidad del sistema.
* Bad, because - Complejidad adicional debido a las comunicaciones entre capas para la comunicación de los microservicios.
* Bad, because - Necesidad de estándares para la buena comunicación entre capas.
* Bad, because - Puede limitar la escalabilidad horizontal de los microservicios.
