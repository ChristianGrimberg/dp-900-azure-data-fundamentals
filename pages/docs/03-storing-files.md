---
document:
  dp900Module: 'Módulo 1'
  dp900Title: 'Análisis sobre el almacenamiento de archivos'
---

# Introduccion

La capacidad de almacenar datos en archivos es un elemento básico de cualquier sistema informático. Los archivos se pueden almacenar en sistemas de archivos locales en el disco duro del equipo personal y en medios extraíbles, como unidades USB, pero en la mayoría de las organizaciones los archivos de datos importantes se almacenan centralmente en algún tipo de sistema de almacenamiento de archivos compartido. Cada vez más, esa ubicación de almacenamiento central se hospeda en la nube, lo que permite un almacenamiento rentable, seguro y de confianza para grandes volúmenes de datos.

El formato de archivo específico que se usa para almacenar datos depende de una serie de factores, entre los que se incluyen los siguientes:

* El tipo de datos que se almacenan (estructurados, semiestructurados o no estructurados).
* Las aplicaciones y los servicios que tendrán que leer, escribir y procesar los datos.
* La necesidad de que los archivos de datos sean legibles para los usuarios o estén optimizados para un almacenamiento y procesamiento eficiente.

## Archivos de texto delimitado

A menudo, los datos se almacenan como texto sin formato con delimitadores de campo y terminadores de fila específicos. El formato más común para los datos delimitados son los _valores separados por comas_ (CSV), en los que los campos están separados por comas y las filas finalizan con un retorno de carro o una nueva línea. Opcionalmente, la primera línea puede incluir los nombres de los campos. Otros formatos comunes incluyen _valores separados por tabulaciones_ (TSV) y delimitados por espacios (en los que se usan tabulaciones o espacios para separar los campos), así como datos de ancho fijo en los que a cada campo se le asigna un número fijo de caracteres. El texto delimitado es una buena opción para los datos estructurados a los que necesita tener acceso una amplia gama de aplicaciones y servicios en un formato legible.

En el ejemplo siguiente se muestran los datos de clientes en formato delimitado por comas:

```csv
FirstName,LastName,Email
Joe,Jones,joe@litware.com
Samir,Nadoy,samir@northwind.com
```
