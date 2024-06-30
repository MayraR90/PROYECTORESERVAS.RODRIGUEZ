# PROYECTORESERVAS.RODRIGUEZ


**PREENTREGA DE PROYECTO:**


**CURSO:SQL**




**ALUMNA:** RODRIGUEZ,MAYRA ALEJANDRA.


**COMISIÓN:** 57190.


**TUTOR:** ARIEL ANNONE.


**DOCENTE:** ANDERSON MICHEL TORRES.


**CONSIGNAS:**

- Descripción de la temática de la base de datos.
- Diagramas de entidad relación de la base de datos.
- Listado de las tablas que comprenden la base de datos, con descripción de cada tabla, listado de campos, abreviaturas de nombres de campos, nombres completos de campos, tipos de datos, tipo de clave (foránea, primaria, índice(s).

**Un archivo .sql que contenga:**

Script en SQL de creación de la base de datos y tablas. Este puede estar publicado en un repositorio github, con lo cual el documento pdf debe contener los links de las publicaciones. 

**Formato**

Aclarar el tipo de archivo en que se espera el desafío. Aclarar que debe tener el nombre “Idea+Apellido”.



Sugerencias

Permitir comentarios en el archivo


**PROBLEMA:**
Se está desarrollando un sistema de gestión de reservas para un club que permita poder  manejar todas las operaciones relacionadas con las mismas.



**DESCRIPCIÓN DEL PROBLEMA:**

- **Gestión de socios y actividades:** Necesitamos una base de datos que nos permita registrar la información de los socios y de las actividades que reservan.


- **Gestión de reservas y disponibilidad:** La base de datos debe permitirnos registrar la disponibilidad de las reservas de cada actividad. Esto nos permitirá evitar conflictos de reservas.


- **Registro de Reservas:** Necesitamos un sistema que pueda registrar de manera detallada cada reserva realizada, incluyendo la fecha y hora de la reserva, el socio que la realizó y  la actividad reservada.


**DESCRIPCIÓN:**
Necesitamos una base de la base para nuestro club que permita registrar las reservas que realizan los socios para las actividades que brindamos  todos los días.

+------------------+        +-----------------------+        +------------------+
|      CLIENTE     |        |       RESERVA         |        |     RESTAURANTE  |
+------------------+        +-----------------------+        +------------------+
| idCliente (PK)   |<>-----o| idReserva (PK)        |o-------| idRestaurante(PK)|
| nombre           |        | idCliente (FK)        |        | nombre           |
| telefono         |        | idMesa (FK)           |        | direccion        |
| correo           |        | idEmpleado (FK)       |        | telefono         |
+------------------+        | idTipoReserva (FK)    |        +------------------+
                            | fecha                 |
                            | cancelacion           |                  |
                            +-----------------------+                  |
                                    |                                  |
                                    |                                  |
                                    v                                  v
+------------------+        +------------------+             +-------------------+
|     Empleado     |        |      Mesa        |             |     Dueno         |
+------------------+        +------------------+             +-------------------+
| idEmpleado (PK)  |        | idMesa (PK)      |             | idDueno (PK)      |
| nombre           |        | idRestaurante(FK)|             | nombre            |
| telefono         |        | capacidad        |             | correo            |
| correo           |        | disponible       |             | telefono          |
| idRestaurante(FK)|        +------------------+             +-------------------+
+------------------+                  |
                             +-------------------+
                             |   TipoReserva     |
                             +-------------------+
                             | idTipoReserva(PK) |
                             | tipo              |
                             +-------------------+
``

+------------------+        +-----------------------+        +------------------+
|      CLIENTE     |        |       RESERVA         |        |     SEDE         |
+------------------+        +-----------------------+        +------------------+          
| idCliente (PK)   |<>-----o| idReserva (PK)        |o-------| idsede(PK)       |
| nombre           |        | idCliente (FK)        |        | nombre           |
| telefono         |        | idMesa (FK)           |        | direccion        |
| correo           |        | idEmpleado (FK)       |        | telefono         |
+------------------+        | idTipoReserva (FK)    |        +------------------+
                            | fecha                 |
                            | cancelacion           |                  |
                            +-----------------------+                  |
                                    |                                  |
                                    |                                  |
                                    v                                  v
+------------------+        +------------------+             +-------------------+
|     Empleado     |        |      Mesa        |             |     Dueno         |
+------------------+        +------------------+             +-------------------+
| idEmpleado (PK)  |        | idMesa (PK)      |             | idDueno (PK)      |
| nombre           |        | idRestaurante(FK)|             | nombre            |
| telefono         |        | capacidad        |             | correo            |
| correo           |        | disponible       |             | telefono          |
| idRestaurante(FK)|        +------------------+             +-------------------+
+------------------+                  |
                             +-------------------+
                             |   TipoReserva     |
                             +-------------------+
                             | idTipoReserva(PK) |
                             | tipo              |
                             +-------------------+

