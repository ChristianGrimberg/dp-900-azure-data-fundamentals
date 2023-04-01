---
document:
  dp900Module: 'Módulo 2'
  dp900Unit: 'Unidad 9'
  dp900Title: 'Análisis de los servicios de datos'
---

# Análisis de los servicios de datos

Microsoft Azure es una plataforma de nube que usan las aplicaciones y la infraestructura de TI de algunas de las organizaciones más grandes del mundo. Incluye numerosos servicios para admitir soluciones en la nube, incluidas cargas de trabajo de datos transaccionales y analíticos.

A continuación se describen algunos de los servicios en la nube que se usan más a menudo para los datos.

> Nota: En este tema se tratan solo algunos de los servicios de datos más usados para soluciones transaccionales y analíticas modernas. Hay disponibles otros servicios.

## Azure SQL

![Azure SQL](../img/azure-sql.png) _Azure SQL_ es el nombre colectivo de una familia de soluciones de bases de datos relacionales basadas en el motor de base de datos de Microsoft SQL Server. Los servicios específicos de Azure SQL incluyen:

* __Azure SQL Database__: se trata de una base de datos de _Plataforma como Servicio_ (PaaS) totalmente administrada y hospedada en Azure.
* __Azure SQL Managed Instance__: es una instancia hospedada de SQL Server con mantenimiento automatizado, que permite una configuración más flexible que Azure SQL Database, pero con más responsabilidad administrativa para el propietario.
* __Máquina virtual de Azure SQL__: consiste en una máquina virtual con una instalación de SQL Server, lo que ofrece una capacidad de configuración máxima con una responsabilidad de administración completa.

Normalmente, los administradores de bases de datos aprovisionan y administran sistemas de bases de datos de Azure SQL para admitir _aplicaciones de línea de negocio_ (LOB) que necesitan almacenar datos transaccionales.

Los ingenieros de datos pueden usar sistemas de bases de datos de Azure SQL como orígenes para canalizaciones de datos que realizan operaciones de _extracción, transformación y carga_ (ETL) para ingerir los datos transaccionales en un sistema analítico.

Los analistas de datos pueden consultar las bases de datos de Azure SQL directamente para crear informes, aunque en organizaciones grandes los datos suelen combinarse con datos de otros orígenes en un almacén de datos analíticos para admitir análisis empresariales.

## Azure Database para bases de datos relacionales de código abierto

![Azure databases](../img/azure-database.png) Azure incluye servicios administrados para sistemas populares de bases de datos relacionales de código abierto, entre los que se incluyen:

* __Azure Database for MySQL__: consiste en un sistema de administración de bases de datos de código abierto fácil de usar que suele emplearse en aplicaciones de pila para _Linux_, _Apache_, _MySQL_ y _PHP_ (_LAMP_).
* __Azure Database for MariaDB__: es un sistema de administración de bases de datos más reciente que han creado los desarrolladores originales de _MySQL_. El motor de base de datos se ha reescrito y se ha optimizado para mejorar el rendimiento. _MariaDB_ ofrece compatibilidad con _Oracle Database_ (otro sistema conocido de administración de bases de datos comerciales).
* __Azure Database for PostgreSQL__: se trata de una base de datos híbrida de objetos relacionales. Una base de datos de PostgreSQL permite almacenar datos en tablas relacionales, pero también tipos de datos personalizados con sus propias propiedades no relacionales.
