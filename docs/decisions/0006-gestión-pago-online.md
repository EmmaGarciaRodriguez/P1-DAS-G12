# Gestión Pago Online

* Status: proposed
* Date: 2024-02-20

## Context and Problem Statement

El sistema debe permitir realizar pagos online, por lo que necesitaremos un módulo que se encargue de esto. Además, el pago debe ser un proceso seguro y fiable.

## Decision Drivers

* RF3.2.1 Pago Online

## Considered Options

* Crear un módulo que permita realizar los pagos
* Implementar una API que haga de pasarela para realizar los pagos

## Decision Outcome

Chosen option: "Implementar una API que haga de pasarela para realizar los pagos", because Garantiza la seguridad en el proceso de pago y más fiabilidad que si lo implementaramos de cero, siendo ésta una solución existente y funcional.
