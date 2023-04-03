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

Al igual que sucede con los sistemas de bases de datos de Azure SQL, los administradores de bases de datos son los responsables de administrar las bases de datos relacionales de código abierto para admitir aplicaciones transaccionales. Dichas bases de datos proporcionan un origen de datos para los ingenieros de datos que crean canalizaciones destinadas a soluciones analíticas, así como para los analistas de datos que crean informes.

## Azure Cosmos DB

![Azure Cosmos DB](../img/cosmos-db.png) Azure Cosmos DB es un sistema de base de datos no relacional (NoSQL) a escala global que admite varias interfaces de programación de aplicaciones (API), lo que permite almacenar y administrar datos como documentos JSON, pares clave-valor, familias de columnas y gráficos.

En algunas organizaciones, los administradores de base de datos pueden aprovisionar y administrar las instancias de Cosmos DB, aunque suelen ser los desarrolladores de software quienes administran el almacenamiento de datos NoSQL como parte de la arquitectura general de la aplicación. A menudo, los ingenieros de datos necesitan integrar orígenes de datos de Cosmos DB en soluciones analíticas empresariales que admitan el modelado y la elaboración de informes por parte de los analistas de datos.

## Azure Storage

![Azure Storage](../img/azure-storage.png) Azure Storage es un servicio básico de Azure que permite almacenar datos en:

* __Contenedores de blobs__: almacenamiento escalable y rentable para archivos binarios.
* __Recursos compartidos de archivos__: recursos compartidos de archivos de red, como es habitual en redes corporativas.
* __Tablas__: almacenamiento de clave-valor para aplicaciones que necesitan leer y escribir valores de datos rápidamente.

Los ingenieros de datos usan Azure Storage para hospedar _lagos de datos_, es decir, almacenamiento de blobs con un espacio de nombres jerárquico que permite organizar los archivos en carpetas en un sistema de archivos distribuido.

## Azure Data Factory

![Azure Data Factory](../img/azure-data-factory.png) Azure Data Factory es un servicio de Azure que permite definir y programar canalizaciones de datos para transferir y transformar datos. Puede integrar las canalizaciones con otros servicios de Azure, lo que le permite ingerir datos de almacenes de datos en la nube, procesar los datos mediante procesos basados en la nube y conservar los resultados en otro almacén de datos.

Los ingenieros de datos usan Azure Data Factory para compilar soluciones de _extracción, transformación y carga_ (ETL) que rellenan almacenes de datos analíticos con datos de sistemas transaccionales de toda la organización.

## Azure Synapse Analytics

![Azure Synapse Analytics](../img/azure-synapse.png) Azure Synapse Analytics es una solución completa y unificada de análisis de datos que proporciona una interfaz de servicio única para varias funcionalidades analíticas, entre las que se incluyen las siguientes:

* __Pipelines__: se basa en la misma tecnología que Azure Data Factory.
* __SQL__: se trata de un motor de base de datos SQL altamente escalable, optimizado para cargas de trabajo de almacenamiento de datos.
* __Apache Spark__: es un sistema de procesamiento de datos distribuidos de código abierto que admite varios lenguajes de programación y API, incluidos Java, Scala, Python y SQL.
* __Azure Synapse Data Explorer__: consiste en una solución de análisis de datos de alto rendimiento que está optimizada para consultas en tiempo real de datos de registro y telemetría mediante el _Lenguaje de Consulta Kusto_ (KQL).

Los ingenieros de datos pueden usar Azure Synapse Analytics para crear una solución de análisis de datos unificada que combine canalizaciones de ingesta de datos, almacenamiento en el almacén de datos y almacenamiento en el lago de datos mediante un único servicio.

Los analistas de datos pueden usar grupos de Spark y SQL mediante cuadernos interactivos para explorar y analizar los datos. Además, pueden aprovechar la integración con servicios como Azure Machine Learning y Microsoft Power BI para crear modelos de datos y extraer información de los datos.

## Azure Databricks

![Azure Databricks](../img/azure-databricks.png) Azure Databricks es una versión integrada de Azure de la popular plataforma Databricks, que combina la plataforma de procesamiento de datos de Apache Spark con la semántica de base de datos SQL y una interfaz de administración integrada para habilitar el análisis de datos a gran escala.

Los ingenieros de datos pueden usar las capacidades de Databricks y Spark para crear almacenes de datos analíticos en Azure Databricks.

Los analistas de datos pueden usar la compatibilidad nativa con cuadernos en Azure Databricks para consultar y visualizar datos en una interfaz basada en web fácil de usar.

## HDInsight de Azure

![HDInsight de Azure](../img/hdinsight.png) Azure HDInsight es un servicio de Azure que proporciona clústeres hospedados en Azure para tecnologías conocidas de procesamiento de macrodatos de código abierto de Apache, entre las que se incluyen las siguientes:

* __Apache Spark__: es un sistema de procesamiento de datos distribuidos que admite varios lenguajes de programación y API, incluidos Java, Scala, Python y SQL.
* __Apache Hadoop__: se trata de un sistema distribuido que usa trabajos de _MapReduce_ para procesar grandes volúmenes de datos de forma eficaz en varios nodos de clúster. Los trabajos de MapReduce pueden escribirse en Java o abstraerse mediante interfaces como Apache Hive, una API basada en SQL que se ejecuta en Hadoop.
* __Apache HBase__: consiste en un sistema de código abierto para consultas y almacenamiento de datos NoSQL a gran escala.
* __Apache Kafka__: es un agente de mensajes para el procesamiento de flujos de datos.
* __Apache Storm__: se trata de un sistema de código abierto para el procesamiento de datos en tiempo real mediante una topología de _spouts_ y _bolts_.

Los ingenieros de datos pueden usar Azure HDInsight para admitir cargas de trabajo de análisis de macrodatos que dependan de varias tecnologías de código abierto.

## Azure Stream Analytics

![Azure Stream Analytics](../img/stream-analytics.png) Azure Stream Analytics es un motor de procesamiento de flujos en tiempo real que captura un flujo de datos de una entrada, aplica una consulta para extraer y manipular los datos del flujo de entrada y escribe los resultados en una salida para su análisis o procesamiento posterior.

Los ingenieros de datos pueden incorporar Azure Stream Analytics en arquitecturas de análisis de datos que capturan datos de streaming para su ingesta en un almacén de datos analíticos o para su visualización en tiempo real.
