---
document:
  dp900Module: 'Módulo 1'
  dp900Unit: 'Unidad 6'
  dp900Title: 'Análisis sobre el procesamiento de datos analíticos'
---

# Análisis sobre el procesamiento de datos analíticos

Normalmente, el procesamiento de datos analíticos se usa con sistemas de solo lectura (o principalmente de lectura) que almacenan grandes volúmenes de datos históricos o de métricas empresariales. Los análisis pueden basarse en una instantánea de los datos en un momento concreto o bajo una serie de instantáneas.

Los detalles específicos de un sistema de procesamiento de datos analítico pueden variar según la solución, pero para una arquitectura común de análisis a escala empresarial tiene el siguiente aspecto:

![Procesamiento tanalítico](../img/06-analytical-processing.png)

1. Los archivos de datos se pueden almacenar en un _lago de datos_ central para analizarlos.
1. Un proceso de _extracción, transformación y carga_ (ETL) permite copiar datos de archivos y bases de datos OLTP en un _almacen de datos_ optimizado para la actividad de lectura. Normalmente, un esquema de almacenamiento de datos se basa en _tablas de hechos_ que contienen los valores numéricos que se quieren analizar (por ejemplo, los importes de ventas), con _tablas de dimensiones relacionadas_ que terminan representando las entidades por las que se quiere medir (por ejemplo, de clientes o productos).
1. Los datos del almacen de datos se pueden agregar y cargar en un modelo de _procesamiento analítico en línea_ (OLAP) o en un cubo. Los valores numéricos agregados (las medidas) en las tablas de hechos se calculan para la intersección de dimensiones a partir de las tablas de dimensiones. Por ejemplo, los ingresos de ventas podrían sumarse por fecha, cliente y producto.
1. Los datos del lago de datos, del almacen de datos y del modelo analítico se pueden consultar para poder generar informes, visualizaciones y paneles.

Los _lagos de datos_ (Data Lake) son comunes en escenarios de procesamiento analítico de datos modernos, en los que se debe recopilar y analizar un gran volumen de datos basado en archivos.

Los _almacenes de datos_ (Data Warehouse) son un recurso establecido para almacenar datos en un esquema relacional optimizado para operaciones de lectura, principalmente con consultas que admiten informes y permiten la visualización de datos. El esquema del almacen de datos puede requerir alguna desnormalización de los datos en un origen de datos OLTP (que introduce cierta duplicación para que las consultas se lleven a cabo con mayor rapidez).

Un modelo OLAP es un tipo de composición de almacenamiento de datos optimizado para cargas de trabajo analíticas. Las adiciones de datos se encuentran en diferentes dimensiones y en distintos niveles, lo que permite rastrearlos agrupando los datos y explorando en profundidad las mismas adiciones en varios niveles jerárquicos; por ejemplo, para buscar el total de ventas por región, por ciudad o por una dirección individual. Dado que los datos de OLAP se agregan previamente, las consultas para devolver los datos sumarizados que contienen se pueden ejecutar rápidamente.

Los diferentes tipos de usuario pueden llevar a cabo el trabajo analítico de datos en distintas fases de la arquitectura en general. Por ejemplo:

* Los científicos de datos pueden trabajar directamente con archivos de datos en un lago de datos para explorar los datos y crear modelos a partir de estos.
* Los analistas de datos pueden consultar tablas directamente en el almacenamiento de datos para generar informes y generar visualizaciones complejas.
* Los usuarios profesionales pueden consumir datos agregados previamente en un modelo analítico como en los informes o en paneles.
