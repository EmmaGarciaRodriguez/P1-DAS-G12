# Gestión Pago Online

* Status: proposed
* Date: 2024-02-20

## Context and Problem Statement

El sistema debe permitir realizar pagos online a los clientes.

## Decision Drivers

* RF3.2.1 Pago Online

## Considered Options

* Implementación de una pasarela de pago propia
* Importar una API externa que realice los pagos a través de una pasarela de pago

## Decision Outcome

Chosen option: "Importar una API externa que realice los pagos a través de una pasarela de pago", because garantiza la seguridad en el proceso de pago y más fiabilidad que si lo implementaramos de cero, siendo ésta una solución existente y funcional.

## Pros and Cons of the Options

### Importar una API externa que realice los pagos a través de una pasarela de pago

Utilizar una API externa que permita realizar pagos online.

* Good, because es una API ya existente y fiable.
* Good, because no hay que implementarla desde cero.
* Bad, because habría que adquirir los permisos necesarios.
