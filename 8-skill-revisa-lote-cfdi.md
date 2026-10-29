---
name: revisa-lote-cfdi
description: Revisa un lote de XML de CFDI de un cliente en México. Lo pasa a una tabla de Excel, cuadra totales, busca duplicados y lo revisa como auditor, con fundamento. Úsala cuando te suban XML de CFDI.
---

# Revisa un lote de CFDI

Sirve para el lote de XML (CFDI 4.0) de gastos o ingresos de un cliente, en
cualquier proyecto. Haz los cuatro pasos en orden y entrega todo en un solo
archivo de Excel para descargar, con una hoja por paso.

## Antes de empezar: pregunta lo que falte

Si no lo sabes por el proyecto o por la conversación, pregunta antes de
revisar, todo en una sola pregunta:

1. Quién es el cliente: el RFC del receptor (o emisor) que se repite en el lote.
2. Su régimen fiscal y si es persona física o moral.
3. El periodo que se revisa (mes y año).
4. Si son gastos (recibidos) o ingresos (emitidos).

Si el contador te dice "ya sabes", infiérelo del lote y dilo en una línea
antes de empezar.

## Paso 1. La tabla

Hoja "Tabla". Una fila por CFDI, con estas columnas: archivo, UUID, fecha,
RFC y nombre del emisor, RFC del receptor, uso del CFDI, método de pago, forma
de pago, subtotal, descuento, IVA trasladado, IVA retenido, ISR retenido y
total. Al final, una fila con los totales.

Lee los datos del XML, no del nombre del archivo. Si un XML no se puede leer,
ponlo en su fila y di por qué.

## Paso 2. La revisión

Hoja "Revisión". Tres cosas, con el archivo y el dato de cada hallazgo:

1. La suma de los totales, y la suma sin duplicados si los hay.
2. Los CFDI duplicados: mismo UUID, aunque el archivo se llame distinto.
3. Los que no cuadran: el total contra subtotal menos descuento más impuestos
   trasladados menos retenidos. Di la diferencia en pesos.

Un CFDI que no cuadra pudo modificarse después de timbrado: recomienda
verificarlo en el portal del SAT con su UUID antes de registrarlo.

## Paso 3. El auditor

Hoja "Hallazgos". Revísalo como lo haría el auditor de un despacho en México.
Señala, como mínimo:

- Lo que impida deducir o acreditar: pagos en efectivo que no se pueden
  deducir (con atención especial al combustible), CFDI a nombre de alguien
  que no es el cliente, uso del CFDI que no corresponde al gasto.
- Lo que obligaba al cliente a retener y no se retuvo (por ejemplo,
  honorarios o arrendamiento de personas físicas pagados por una persona
  moral).
- Método y forma de pago que no casan (PUE con forma 99, PPD sin complemento
  de pago).
- Lo que esté fuera del periodo.
- Cualquier otro dato que no sea consistente, aunque no esté en esta lista.

Para cada hallazgo: archivo, qué pasa, fundamento (artículo, fracción y ley)
y qué harías. Ordena de mayor a menor riesgo.

## Paso 4. El resumen

En el chat, no en el Excel: tres renglones con lo más importante y el enlace
al archivo. El detalle vive en las hojas.

## Reglas

- Norma vigente en México: LISR, LIVA, CFF, sus reglamentos y la Resolución
  Miscelánea Fiscal. Cita artículo y fracción.
- Si no tienes el fundamento con certeza, o la norma pudo cambiar, dilo y no
  lo inventes.
- Señalas, clasificas y priorizas. No concluyes por el contador: la decisión
  y la firma son suyas.
- Montos en pesos mexicanos, con separador de miles.
- Si ves datos que no hacen falta para revisar (direcciones, cuentas
  bancarias completas), no los repitas en la respuesta.
