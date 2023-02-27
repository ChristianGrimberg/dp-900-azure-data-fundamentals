---
document:
  dp900Module: 'Módulo 1'
  dp900Title: 'Análisis sobre el procesamiento de datos transaccionales'
---

# Análisis sobre el procesamiento de datos transaccionales

Un sistema de procesamiento de datos transaccional es lo que la mayoría de los usuarios considera la función principal de la informática empresarial. Un sistema transaccional registra las __transacciones__ que encapsulan eventos específicos de los que la organización quiere realizar un seguimiento. Una transacción podría ser financiera, como el movimiento de dinero entre cuentas de un sistema bancario, o bien podría formar parte de un sistema de venta al por menor y llevar un seguimiento de los pagos de bienes y servicios de los clientes. Piense en una transacción como una unidad de trabajo pequeña y discreta.

Los sistemas transaccionales suelen ser de gran volumen, a veces, controlan muchos millones de transacciones en un solo día y se debe poder acceder a los datos que se procesan con mucha rapidez. El trabajo que realizan los sistemas transaccionales a menudo se conoce como _Procesamiento de Transacciones en Línea_ (OLTP).

![Procesamiento transaccional](../img/05-transactional-processing.png)

Las soluciones OLTP se basan en un sistema de base de datos en el que el almacenamiento de datos está optimizado tanto para las operaciones de lectura como para las de escritura, con el fin de admitir cargas de trabajo transaccionales en las que se crean, recuperan, actualizan y eliminan registros de datos (a menudo denominadas _Operaciones CRUD_). Estas operaciones se aplican transaccionalmente, de una forma que garantiza la integridad de los datos almacenados en la base de datos. Para ello, los sistemas OLTP aplican transacciones que admiten la denominada semántica _ACID_:

* __Atomicidad__: cada transacción se trata como una unidad única, la cual se completa correctamente o produce un error general. Por ejemplo, una transacción que conlleve el adeudo de fondos de una cuenta y el abono de la misma cantidad en otra debe completar ambas acciones. Si alguna de las acciones no se puede completar, se debe producir un error en la otra.
* __Coherencia__: las transacciones solo pueden pasar los datos de la base de datos de un estado válido a otro. Para continuar con el ejemplo anterior del adeudo y el abono, el estado completado de la transacción debe reflejar la transferencia de fondos de una cuenta a la otra.
* __Aislamiento__: las transacciones simultáneas no pueden interferir entre sí y deben dar lugar a un estado coherente de la base de datos. Por ejemplo, mientras la transacción para transferir fondos de una cuenta a otra está en proceso, otra transacción que comprueba el saldo de las cuentas debe devolver resultados coherentes. Es decir, la transacción de comprobación del saldo no puede recuperar un valor para una cuenta que refleje el saldo antes de la transferencia y un valor para la otra cuenta que refleje el saldo después de la transferencia.
* __Durabilidad__: cuando se ha confirmado una transacción, permanece confirmada. Una vez que la transacción de transferencia de la cuenta se ha completado, los saldos revisados de las cuentas se conservan, de modo que, incluso si el sistema de base de datos se desactiva, la transacción confirmada se refleje cuando se vuelva a activar.

Los sistemas OLTP suelen usarse para admitir aplicaciones activas que procesan datos empresariales, a menudo denominadas _Aplicaciones de Negocio en Línea_ (LOB).
