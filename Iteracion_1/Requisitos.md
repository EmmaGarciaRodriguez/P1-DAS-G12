<h1>Requisitos<h1>
<details>
<summary><h3>RF1 Arquitectura Microservicios</h3></summary>

- Se desea migrar una arquitectura monolítica a una basada en microservicios donde existen dos tipos de clientes (PC y Móvil) que acceden a la lógica de negocio del sistema mediante protocolo HTTP/REST a través de un elemento del tipo API Gateway. Además, deberá existir una capa de acceso a datos donde se almacenen los datos de la compañía correspondientes a los pedidos y clientes.
</details>

<details>
<summary><h3>RF2 Información clientes y pedidos**</h3></summary>

- El sistema debe tener una base de datos para almacenar los datos de los clientes y otra para los datos de los pedidos.
</details>

<details>
<summary><h3>RF3 Lógica de negocio</h3></summary>

- La lógica de negocio de la empresa cuenta con los siguientes módulos: clientes, pedidos, repartos y rutas, y estadísticas.

<details>
<summary><h4>RF3.1 Módulo Clientes</h4></summary>

- A través de este módulo el sistema debe permitir el acceso a la siguiente información de los usuarios: identificador, nombre, apellidos, email y teléfono móvil.
</details>

<details>
<summary><h4>RF3.2 Módulo Pedidos</h4></summary>

- El sistema debe tener un módulo que permita a los clientes realizar compras. Además, el sistema debe permitir realizar el mismo pedido un máximo de 3 veces.
<details>
<summary>RF3.2.1 Pago Online</summary>

- Este módulo debe contar con una funcionalidad que permita el pago online a los clientes.
</details>
</details>

<details>
<summary><h4>RF3.3 Módulo Reparto y rutas</h4></summary>

- Este componente complejo cuenta con una gran funcionalidad que es necesario desacoplar y gestiona el reparto de las flotas de transporte a los clientes y las rutas de los camiones. La gestión cuenta con 2 algoritmos de optimización que se seleccionan en función de la demora del camión.

<details>
<summary>RF3.3.1 Incidencias</summary>

- Se deben reportar las incidencias durante el reparto. Las incidencias pueden ser de tres tipos: camión averiado, demora, no entrega de pedido.
</details>
</details>

<details>
<summary><h3>RF3.4 Módulo Estadísticas</h3></summary>

- El sistema cuenta con un módulo de estadísticas que proporciona información valiosa sobre el estado de los pedidos y la situación en tiempo real de los camiones. Las estadísticas proporcionan también información de clientes.
</details>

</details>

<details>
<summary><h3>RF4 Notificación del estado del pedido</h3></summary>

- El módulo reparto y rutas debe poder notificar a los clientes el estado de su pedido vía mensajes al teléfono móvil y otros posibles canales de comunicación.
</details>
