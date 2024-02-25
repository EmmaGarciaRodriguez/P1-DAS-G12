# Actualización Base de Datos

* Status: proposed
* Date: 2024-02-25


## Considered Options

* Uso de Microsoft ODBC Driver for SQL Server
* Uso del driver JDBC con MySQL 8.0

## Decision Outcome

Chosen option: "Uso del driver JDBC con MySQL 8.0", because es compatible para múltiples plataformas y es el que mejor se adapta al entorno de desarrollo y las necesidades del sistema.

## Pros and Cons of the Options

### Uso de Microsoft ODBC Driver for SQL Server

* Good, because El controlador ODBC de Microsoft está específicamente optimizado para trabajar con SQL Server
* Bad, because Su soporte principal está destinado a entornos Windows, lo cual puede limitar la portabilidad de las aplicaciones.

### Uso del driver JDBC con MySQL 8.0

* Good, because JDBC es un estándar de Java, por lo que es compatible con múltiples plataformas.
* Good, because JDBC ofrece un rendimiento optimizado para MySQL.
* Bad, because JDBC se limita únicamente a java, por lo que sólamente puede integrarse en aplicaciones desarrolladas en java.

## Links

* https://www.ibm.com/docs/es/i/7.1?topic=programming-toolbox-java-jdbc-driver
* https://learn.microsoft.com/es-es/sql/connect/odbc/microsoft-odbc-driver-for-sql-server?view=sql-server-ver16
