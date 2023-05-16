---
document:
  dp900Module: 'Módulo 3'
  dp900Unit: 'Unidad 2'
  dp900Title: 'Información sobre los datos relacionales'
---

# Información sobre los datos relacionales

En una base de datos relacional, las colecciones de entidades del mundo real se modelan en forma de _tablas_. Una entidad puede ser cualquier elemento para quien necesite registrar la información; por lo general, se trata de objetos y eventos importantes. Por ejemplo, en un sistema de venta al por menor, puede crear tablas para clientes, productos, pedidos y artículos de línea de un pedido. Una tabla contiene filas, y cada fila representa una instancia única de una entidad. En este escenario de venta al por menor, cada fila de la tabla de clientes contiene los datos de un solo cliente, cada fila de la tabla de productos define un único producto, cada fila de la tabla de pedidos representa un pedido realizado por un cliente y cada fila de la tabla de artículos en línea representa un producto que se ha incluido en un pedido.

![Tablas relacionales](../img/relational-tables.png)

Las tablas relacionales son un formato para los datos estructurados y cada fila de una tabla tiene las mismas columnas, aunque en algunos casos no todas las columnas necesitan tener un valor. Por ejemplo, una tabla de clientes puede incluir una columna __MiddleName__, que podría estar vacía (o ser `NULL`) para las filas que representan a los clientes que no tienen un segundo nombre o cuyo segundo nombre se desconoce.

Cada columna almacena los datos de un tipo de datos específico. Por ejemplo, una columna __Email__ de una tabla __Customer__ probablemente se definiría para almacenar datos basados en caracteres (texto), que podrían ser de longitud fija o variable. Una columna __Price__ de una tabla __Product__ podría definirse para almacenar datos numéricos decimales, mientras que una columna __Quantity__ de una tabla __Order__ podría estar restringida a valores numéricos enteros. Una columna __OrderDate__ de la misma tabla __Order__ se definiría para almacenar valores de fecha y hora. Los tipos de datos disponibles que se pueden usar al definir una tabla dependen del sistema de base de datos que se use, aunque hay tipos de datos estándar definidos por el _American National Standards Institute_ (ANSI) que son compatibles con la mayoría de los sistemas de base de datos.

[Unidad siguiente: [Unidad siguiente: Comprensión de la normalización](3-03-normaliation.md)
