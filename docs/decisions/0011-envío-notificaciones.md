# Envío notificaciones

* Status: proposed
* Date: 2024-03-01

## Context and Problem Statement

El Módulo reparto y rutas debe poder notificar a los clientes en todo momento del estado de su pedido vía mensajes al teléfono móvil así como otros posibles canales de comunicación.

## Decision Drivers

* RF4 Notificación del estado del pedido

## Considered Options

* Una clase Notificaciones que tenga una interfaz para diferenciar el canal de notificación
* La clase Gestor Pedidos y Rutas se encarga de enviar las notificaciones al cliente

## Decision Outcome

Chosen option: "La clase Gestor Pedidos y Rutas se encarga de enviar las notificaciones al cliente", because es una solución más sencilla e igual de completa que la otra para cumplir el requisito de envío de notificaciones.

## Pros and Cons of the Options

### Una clase Notificaciones que tenga una interfaz para diferenciar el canal de notificación

Una clase notificaciones la cual tendría una interfaz que implementarían las notificaciones vía móvil y las notificaciones vía redes sociales, por ejemplo

* Good, because Permite desacoplar la funcionalidad de otras clases
* Bad, because Aumenta significativamente la complejidad

### La clase Gestor Pedidos y Rutas se encarga de enviar las notificaciones al cliente

El módulo Repartos y Rutas cuenta con una clase Gestor Pedidos y Rutas que se ocupa del envío de notificaciones respecto del pedido al cliente correspondiente.

* Good, because es una solución sencilla y completa para el problema de diseño
* Good, because no aumenta nada o casi nada la complejidad del sistema
