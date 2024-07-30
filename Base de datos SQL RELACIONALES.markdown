# Comandos SQL y Conceptos Esenciales

## Conceptos Básicos de SQL
- **Bases de datos (Databases)**
- **Tablas (Tables)**
- **Filas (Rows/Records)**
- **Columnas (Columns/Fields)**
- **Schemas**
- **Tipos de Datos (Data Types)**
  - INTEGER
  - VARCHAR
  - DATE
  - BOOLEAN
  - FLOAT, etc.

## DDL (Data Definition Language)
- **CREATE TABLE**: Crear una tabla.
- **ALTER TABLE**: Modificar la estructura de una tabla.
- **DROP TABLE**: Eliminar una tabla.
- **TRUNCATE TABLE**: Eliminar todos los registros de una tabla sin eliminar la estructura de la tabla.
- **CREATE INDEX**: Crear un índice en una tabla.
- **DROP INDEX**: Eliminar un índice en una tabla.
- **CREATE VIEW**: Crear una vista.
- **ALTER VIEW**: Modificar una vista.
- **DROP VIEW**: Eliminar una vista.

## DML (Data Manipulation Language)
- **SELECT**: Consultar y recuperar datos de tablas.
- **INSERT INTO**: Agregar nuevos registros a una tabla.
- **UPDATE**: Modificar datos existentes en una tabla.
- **DELETE**: Eliminar registros de una tabla.
- **MERGE**: Insertar, actualizar o eliminar registros basados en una fuente de datos.

## DCL (Data Control Language)
- **GRANT**: Otorgar permisos a usuarios sobre objetos de la base de datos.
- **REVOKE**: Revocar permisos otorgados a usuarios.

## TCL (Transaction Control Language)
- **BEGIN TRANSACTION**: Iniciar una transacción.
- **COMMIT**: Guardar permanentemente los cambios realizados en una transacción.
- **ROLLBACK**: Deshacer los cambios realizados en una transacción.
- **SAVEPOINT**: Crear puntos de restauración dentro de una transacción.

## Cláusulas
- **SELECT**
- **FROM**
- **WHERE**: Filtrar filas que cumplen una condición.
- **ORDER BY**: Ordenar las filas resultantes en orden ascendente o descendente.
- **GROUP BY**: Agrupar filas que tienen el mismo valor en columnas especificadas.
- **HAVING**: Filtrar grupos basados en una condición.
- **LIMIT/OFFSET**: Limitar y desplazar el número de filas devueltas.
- **JOIN**: Combinar filas de dos o más tablas basadas en una columna relacionada.
  - **INNER JOIN**: Devuelve filas que tienen coincidencias en ambas tablas.
  - **LEFT JOIN (LEFT OUTER JOIN)**: Devuelve todas las filas de la tabla izquierda y las filas coincidentes de la tabla derecha.
  - **RIGHT JOIN (RIGHT OUTER JOIN)**: Devuelve todas las filas de la tabla derecha y las filas coincidentes de la tabla izquierda.
  - **FULL JOIN (FULL OUTER JOIN)**: Devuelve filas cuando hay una coincidencia en una de las tablas.
  - **CROSS JOIN**: Devuelve el producto cartesiano de ambas tablas.
  - **SELF JOIN**: Una tabla se une a sí misma.

## Operadores
- **Aritméticos**: +, -, *, /, % (módulo).
- **Comparación**: =, >, <, >=, <=, <>, BETWEEN, LIKE, IN.
- **Lógicos**: AND, OR, NOT.
- **IS NULL/IS NOT NULL**: Verificar si un valor es NULL o no NULL.

## Funciones

### **Funciones de Agregado**
- **COUNT()**: Contar filas.
- **SUM()**: Sumar valores.
- **AVG()**: Calcular el promedio.
- **MIN()**: Obtener el valor mínimo.
- **MAX()**: Obtener el valor máximo.
- **GROUP_CONCAT()**: Concatenar valores de un grupo en una sola cadena (MySQL).
- **STRING_AGG()**: Concatenar valores de un grupo en una sola cadena (PostgreSQL, SQL Server).
- **VARIANCE()**: Calcular la varianza de los valores.
- **STDDEV()**: Calcular la desviación estándar de los valores.
- **MEDIAN()**: Calcular la mediana de los valores (puede no estar disponible en todos los DBMS).

### **Funciones de Cadena**
- **CONCAT()**: Concatenar cadenas.
- **SUBSTRING()**: Extraer una subcadena.
- **CHAR_LENGTH()**: Obtener la longitud de una cadena.
- **UPPER()**: Convertir a mayúsculas.
- **LOWER()**: Convertir a minúsculas.
- **REPLACE()**: Reemplazar una subcadena en una cadena.
- **TRIM()**: Eliminar espacios en blanco del inicio y final de una cadena.
- **LTRIM()**: Eliminar espacios en blanco del inicio de una cadena.
- **RTRIM()**: Eliminar espacios en blanco del final de una cadena.
- **LEFT()**: Extraer un número específico de caracteres del inicio de una cadena.
- **RIGHT()**: Extraer un número específico de caracteres del final de una cadena.
- **POSITION()**: Encontrar la posición de una subcadena dentro de una cadena.
- **CHARINDEX()**: Encontrar la posición de una subcadena dentro de una cadena (SQL Server).
- **FORMAT()**: Formatear una cadena según un formato especificado (puede variar entre DBMS).
- **SPLIT()**: Dividir una cadena en una tabla de resultados (SQL Server, PostgreSQL).
- **REVERSE()**: Invertir el orden de los caracteres en una cadena.

### **Funciones de Fecha y Hora**
- **CURRENT_DATE**: Obtener la fecha actual.
- **CURRENT_TIME**: Obtener la hora actual.
- **NOW()**: Obtener la fecha y hora actuales.
- **CURDATE()**: Obtener la fecha actual (MySQL).
- **CURTIME()**: Obtener la hora actual (MySQL).
- **DATEADD()**: Añadir un intervalo a una fecha.
- **DATEDIFF()**: Calcular la diferencia entre fechas.
- **TIMEDIFF()**: Calcular la diferencia entre tiempos.
- **DATE_TRUNC()**: Redondear una fecha a una precisión específica (como año, mes, día).
- **EXTRACT()**: Extraer una parte específica de una fecha o hora (como año, mes, día).
- **MONTH()**: Obtener el mes de una fecha.
- **DAY()**: Obtener el día del mes de una fecha.
- **YEAR()**: Obtener el año de una fecha.
- **HOUR()**: Obtener la hora de un valor de tiempo.
- **MINUTE()**: Obtener los minutos de un valor de tiempo.
- **SECOND()**: Obtener los segundos de un valor de tiempo.
- **TIMESTAMPADD()**: Añadir un intervalo a una marca de tiempo.
- **TIMESTAMPDIFF()**: Calcular la diferencia entre dos marcas de tiempo.
- **TO_DATE()**: Convertir una cadena de texto a una fecha.
- **TO_CHAR()**: Convertir un valor a una cadena de texto con formato.
- **TO_TIMESTAMP()**: Convertir una cadena de texto a una marca de tiempo.

### **Funciones de Conversión**
- **CAST()**: Convertir un tipo de dato a otro.
- **CONVERT()**: Similar a CAST, pero con más opciones.
- **TO_NUMBER()**: Convertir una cadena de texto a un número (Oracle).
- **TRY_CAST()**: Intentar convertir un tipo de dato, devolviendo NULL si falla (SQL Server).

### **Funciones de Ventana**
- **ROW_NUMBER()**: Asignar un número único a cada fila dentro de una partición.
- **RANK()**: Asignar un rango a cada fila dentro de una partición.
- **DENSE_RANK()**: Asignar un rango denso a cada fila dentro de una partición.
- **NTILE()**: Dividir un conjunto de resultados en un número específico de grupos.
- **LEAD()**: Acceder al valor de una fila siguiente en una partición.
- **LAG()**: Acceder al valor de una fila anterior en una partición.
- **FIRST_VALUE()**: Obtener el primer valor en una partición.
- **LAST_VALUE()**: Obtener el último valor en una partición.
- **CUME_DIST()**: Calcular la distribución acumulativa de una fila dentro de su partición.
- **PERCENT_RANK()**: Calcular el rango porcentual de una fila dentro de su partición.
- **NTH_VALUE()**: Obtener el enésimo valor en una partición.
- **PERCENTILE_CONT()**: Calcular el percentil continuo en una partición.

### **Funciones de Agregado con Condición**
- **SUM(CASE WHEN condition THEN value ELSE 0 END)**: Sumar valores condicionados.
- **COUNT(CASE WHEN condition THEN 1 END)**: Contar filas que cumplen una condición.



## Integridad y Relaciones
- **Primary Key**: Clave primaria para identificar de manera única cada fila.
- **Foreign Key**: Clave foránea para establecer una relación entre tablas.
- **Unique Key**: Asegura que todos los valores en una columna sean únicos.
- **Not Null**: Asegura que una columna no pueda tener valores NULL.
- **Default**: Proporciona un valor predeterminado para una columna.
- **Check Constraints**: Restringe los valores que se pueden insertar en una columna.

## Índices y Optimización
- **B-Tree Index**: Índice basado en árboles balanceados.
- **Hash Index**: Índice basado en hash.
- **Bitmap Index**: Índice que utiliza un bitmap para cada valor único.
- **Clustered Index**: Índice que determina el orden físico de los datos en la tabla.
- **Non-clustered Index**: Índice que no afecta el orden físico de los datos.
- **Index Scan**: Escaneo de índice.
- **Index Seek**: Búsqueda específica en un índice.

## Procedimientos Almacenados y Triggers
- **CREATE PROCEDURE**: Crear un procedimiento almacenado.
- **ALTER PROCEDURE**: Modificar un procedimiento almacenado.
- **DROP PROCEDURE**: Eliminar un procedimiento almacenado.
- **CREATE TRIGGER**: Crear un trigger.
- **ALTER TRIGGER**: Modificar un trigger.
- **DROP TRIGGER**: Eliminar un trigger.

## Vistas y Materialización
- **Vistas (Views)**: Consultas almacenadas que pueden ser consultadas como tablas.
- **Vistas Materializadas (Materialized Views)**: Vistas que almacenan datos físicamente para mejorar el rendimiento de las consultas.

## Herramientas de Gestión y Administración
- **SQL Server Management Studio (SSMS)**
- **pgAdmin**
- **MySQL Workbench**
- **Oracle SQL Developer**

## Conocimiento de Sistemas de Gestión de Bases de Datos (DBMS)
- **MySQL**
- **PostgreSQL**
- **Microsoft SQL Server**
- **Oracle Database**
- **SQLite**
- **MariaDB**

## Administración de la Base de Datos
- **Backup y Restore**: Respaldar y restaurar bases de datos.
- **Replicación**: Duplicar datos de una base de datos a otra.
- **Sharding**: Dividir una base de datos en partes más pequeñas.
- **Particionamiento**: Dividir grandes tablas en partes más pequeñas.

## Otros Términos y Conceptos
- **Normalization**: Proceso para eliminar redundancia en el diseño de bases de datos.
- **Denormalization**: Introducir redundancias para mejorar rendimiento.
- **ACID Properties**: Propiedades de transacciones (Atomicidad, Consistencia, Aislamiento, Durabilidad).
- **ER Diagrams**: Diagramas de entidad-relación para modelar bases de datos.
- **Data Warehousing**: Almacenamiento de datos a gran escala para análisis.
- **ETL Processes (Extract, Transform, Load)**: Procesos para extraer, transformar y cargar datos en un almacén de datos.
- **Big Data Integration**: Integración y manejo de grandes volúmenes de datos.
