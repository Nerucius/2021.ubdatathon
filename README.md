# Universityhack 2021 DATATHON

More info at: https://www.cajamardatalab.com/datathon-cajamar-universityhack-2021/retos/predictivo/

**NOTE**: After cloning, unzip the file data.zip in the data folder

## El objetivo

> Para cualquier e-commerce es muy importante tener disponibles, siempre que sea posible, aquellos productos que reclaman sus consumidores, el abastecimiento de la demanda es imprescindible para dar un buen servicio al cliente.

> Para poder garantizar dicha disponibilidad hay que tener en cuenta dos factores que convierten lo anterior en un reto: no se puede incurrir en rotura de stock (situación en la que la demanda de producto resulta ser superior a las previsiones y se presentan dificultades de abastecimiento en tiempo y forma adecuados) pero tampoco excederse en el aprovisionamiento de unidades de producto con una demanda insuficiente, puesto que requieren un espacio de almacenamiento que es limitado. Por tanto, se necesita una situación de equilibrio que garantice que las desviaciones con respecto a las ventas reales sean mínimas, pero sin incurrir en rotura, puesto que esto tiene impacto directo en la satisfacción de los clientes.

## El dataset

> El dataset integra la información de las ventas y atributos de producto para las fechas comprendidas entre 01/06/2015 y el 30/09/2016.

### FICHEROS

**Dataset "Modelar_UH2021.txt"**: Con este fichero deberás construir un modelo predictivo que permita estimar las ventas por producto y día. Datos entre 01/06/2015 y el 30/09/2016.

**Dataset "Estimar_UH2021.txt"**: El modelo generado lo aplicarás a los datos de este fichero, de modo que calcules, para cada producto y día, el número de artículos vendidos más probable. Datos entre 01/10/2016 y el 31/12/2016.

### VARIABLES

- **Fecha**: momento del tiempo en el que se produce el evento.
- **Id**: número identificador del artículo.
- **Visitas**: número de veces que ha sido visualizada la ficha de un producto dado para un día concreto. Remarcamos que puede darse el caso en el que las visitas sean inferiores a las compras de ese mismo día, siempre que el producto que se ha comprado estuviera previamente añadido al carrito o se haya añadido desde la opción del recomendador sin pasar por ficha de producto.
- **Categoría_uno**: categoría de producto nivel uno.
- **Categoría_dos**: segundo nivel de agrupación para cada producto que precede a la de nivel uno.
- **Estado**: situación en la que se encuentra el producto. Esta variable toma 3 posibles valores para el dataset Modelar_UH2021:
	- **Rotura**: no hay stock físico disponible para servir en nuestros almacenes.
	- **Tránsito**: no hay stock físico en nuestros almacenes, pero está pendiente de entrega inminente desde proveedor.
	- **No Rotura**: hay stock físico disponible en nuestros almacenes.
	Para el dataset Estimar_UH2021 todas las variables aparecen con el estado Tránsito o No Rotura.
- **Precio**: indica el precio unitario al que se realiza la transacción. Cuando su valor es nulo, ha de ser completado con el precio anterior temporalmente más cercano para cada artículo.
- **Día atípico**: toma los siguientes valores:
	- 0: si estamos fuera de fechas con comportamiento atípico.
	- 1: si estamos en un periodo con una demanda más alta de lo habitual.
	- -1: si estamos en un periodo con una demanda más baja de lo habitual.
- **Campaña**: esta variable nos indica para las campañas principales, si el producto estaba en promoción o no en una fecha determinada.
- **Antigüedad**: días transcurridos desde la entrada en catálogo de cada producto.
- **Unidades vendidas**: variable a predecir. Nos indica las unidades vendidas para cada día y cada artículo.

### FORMATO Y ESTRUCTURA
Los datasets con formato txt tienen como estructura:

Nombres de campo: Incluidos en la cabecera.
Separador: "|"
Codificación: UTF-8.

### DATASET RESPUESTA

Se denominará “Equipo_UH2021.txt” donde Equipo será el nombre del equipo con el que te has inscrito y constará de tres columnas que corresponden a las variables:

Fecha: momento del tiempo en el que se produce el evento.
Id: número identificador del artículo.
Unidades vendidas: variable a predecir.
