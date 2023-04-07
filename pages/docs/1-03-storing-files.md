---
document:
  dp900Module: 'Módulo 1'
  dp900Unit: 'Unidad 3'
  dp900Title: 'Análisis sobre el almacenamiento de archivos'
---

# Análisis sobre el almacenamiento de archivos

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

## Notación de objetos JavaScript (JSON)

JSON es un formato omnipresente en el que se usa un esquema de documento jerárquico para definir entidades de datos (objetos) que tienen varios atributos. Cada atributo puede ser un objeto (o una colección de objetos), lo que hace de JSON un formato flexible adecuado tanto para datos estructurados como semiestructurados.

En el ejemplo siguiente se muestra un documento JSON que contiene una colección de clientes. Cada cliente tiene tres atributos (_firstName_, _lastName_ y _contact_) y el atributo _contact_ contiene una colección de objetos que representan uno o varios métodos de contacto (correo electrónico o teléfono). Tenga en cuenta que los objetos se incluyen entre llaves (`{..}`) y las colecciones se incluyen entre corchetes (`[..]`). Los atributos se representan mediante pares _nombre:valor_ y se separan por comas (`,`).

```json
{
  "customers":
  [
    {
      "firstName": "Joe",
      "lastName": "Jones",
      "contact":
      [
        {
          "type": "home",
          "number": "555 123-1234"
        },
        {
          "type": "email",
          "address": "joe@litware.com"
        }
      ]
    },
    {
      "firstName": "Samir",
      "lastName": "Nadoy",
      "contact":
      [
        {
          "type": "email",
          "address": "samir@northwind.com"
        }
      ]
    }
  ]
}
```

## Lenguaje de marcado extensible (XML)

XML es un formato de datos legible popular en la década de 1990 y 2000. En gran medida lo ha reemplazado el formato JSON, siendo menos detallado, pero todavía hay algunos sistemas que usan XML para representar los datos. XML usa etiquetas entre corchetes angulares (`../`) para definir elementos y atributos, como se muestra en este ejemplo:

```xml
<Customers>
  <Customer name="Joe" lastName="Jones">
    <ContactDetails>
      <Contact type="home" number="555 123-1234"/>
      <Contact type="email" address="joe@litware.com"/>
    </ContactDetails>
  </Customer>
  <Customer name="Samir" lastName="Nadoy">
    <ContactDetails>
      <Contact type="email" address="samir@northwind.com"/>
    </ContactDetails>
  </Customer>
</Customers>
```

## Objeto binario grande (BLOB)

En última instancia, todos los archivos se almacenan como datos binarios (1 y 0), pero en los formatos legibles que se describen anteriormente, los _bytes_ de datos binarios se asignan a caracteres imprimibles (normalmente a través de un esquema de codificación de caracteres como ASCII o Unicode). Aun así, algunos formatos de archivo, especialmente para los datos no estructurados, almacenan los datos como datos binarios sin formato que las aplicaciones deben interpretar y representar. Los tipos comunes de datos almacenados como datos binarios incluyen imágenes, vídeo, audio y documentos específicos de aplicaciones.

Cuando se trabaja con datos de este tipo, los profesionales de datos suelen hacer referencia a estos archivos de datos como BLOB (_objetos binarios grandes_).

## Formatos de archivo optimizados

Aunque los formatos legibles para datos estructurados y semiestructurados pueden ser útiles, normalmente no están optimizados para el procesamiento o el espacio de almacenamiento. Con el paso del tiempo, se han desarrollado algunos formatos de archivo especializados que permiten la compresión, la indexación y un almacenamiento y procesamiento eficiente.

Entre los formatos de archivo optimizados más habituales que puede ver se incluyen _Avro_, _ORC_ y _Parquet_:

* __Avro__ es un formato basado en filas creado por _Apache_. Cada registro contiene un encabezado que describe la estructura de los datos en ese registro. Este encabezado se almacena como JSON. Los datos, por su parte, se almacenan como información binaria. Una aplicación usa la información del encabezado para analizar los datos binarios y extraer los campos que contienen. Avro es un formato adecuado para comprimir datos y reducir los requisitos de almacenamiento y ancho de banda de red.
* __ORC__ (formato de columnas de filas optimizadas) organiza los datos en columnas en lugar de en filas. Lo desarrolló _HortonWorks_ para optimizar las operaciones de lectura y escritura en _Apache Hive_ (Hive es un sistema de almacen de datos que admite un añadido rápido de los datos y consultas en grandes conjuntos de datos). Un archivo ORC contiene franjas de datos. Cada franja contiene los datos de una columna o de un conjunto de columnas. Una franja contiene un índice de las filas de dicha franja, los datos de cada fila y un pie de página que contiene información estadística (_count_, _sum_, _max_, _min_, etcétera) de cada columna.
* __Parquet__ es otro formato de datos en columnas creado por _Cloudera_ y _Twitter_. Un archivo Parquet contiene grupos de filas. Los datos de cada columna se almacenan juntos en el mismo grupo de filas. Cada grupo de filas contiene uno o varios fragmentos de datos. Un archivo Parquet incluye metadatos que describen el conjunto de filas que hay en cada fragmento. Una aplicación puede usar estos metadatos para localizar rápidamente el fragmento correcto para un conjunto determinado de filas y, a continuación, para recuperar los datos de las columnas especificadas relativas a esas filas. Parquet destaca por almacenar y procesar tipos de datos anidados de forma eficaz. Admite esquemas de compresión y codificación muy eficaces.

[Unidad siguiente: Análisis sobre bases de datos](04-databases.md)
