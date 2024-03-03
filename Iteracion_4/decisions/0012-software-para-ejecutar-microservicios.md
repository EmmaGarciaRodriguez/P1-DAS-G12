# Software para ejecutar microservicios

* Status: proposed
* Date: 2024-03-01

## Context and Problem Statement

Se necesita un software capaz de ejecutar el microservicio de Estadísticas.

## Considered Options

* Utilizar Azure Kubernetes Service (AKS)
* Utilizar AWS ECS (Amazon Elastic Container Service)

## Decision Outcome

Chosen option: "Utilizar Azure Kubernetes Service", because Azufre puede ofrecer una combinación de integración de servicios, escalabilidad, seguridad, disponibilidad global y capacidades analíticas que son fundamentales para el éxito de aplicaciones con características como la que se desea desarrollar.

## Pros and Cons of the Options

### Utilizar Azure Kubernetes Service

* Good, because Facilita el despliegue, la gestión y escalabilidad de aplicaciones.
* Good, because Soporte para múltiples plataformas.
* Good, because Alta disponibilidad y facilidad de uso.
* Bad, because Puede generar un bloqueo a la infraestructura de Azure, lo que puede dificultar la migración a otros proveedores de servicios en la nube en el futuro.

### Utilizar AWS ECS

* Good, because Integración con otros servicios de AWS.
* Bad, because Complejidad de configuración inicial.
* Bad, because Puede tener algunas limitaciones en términos de funcionalidades avanzadas y flexibilidad en la gestión de contenedores.
