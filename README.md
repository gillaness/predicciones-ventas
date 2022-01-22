# Predicción Ventas

El presente proyecto consiste en lograr generar un modelo que permita predecir las ventas de distintos productos en una tienda en particular.
Para ello contamos con los siguientes datos:


|Nombre de la variable| Descripción|
|-|-|
|Item_Identifier|ID único de producto|
|Item_Weight|Peso del Producto|
|Item_Fat_Content| Si el producto es bajo en grasas o regular|
|Item_Visibility| El porcentaje del área de exhibición total de todos los productos en una tienda asignado al producto en particular|
|Item_Type|La categoría a la que pertenece el producto|
|Item_MRP|Precio minorista máximo (precio de lista) del producto|
|Outlet_Identifier|ID único de tienda|
|Outlet_Establishment_Year|El año en el que se estableció la tienda.|
|Outlet_Size|El tamaño de la tienda en términos de superficie cubierta|
|Outlet_Location_Type|El tipo de área en la que se encuentra la tienda|
|Outlet_Type|Si el punto de venta es una tienda de comestibles o algún tipo de supermercado|
|Item_Outlet_Sales|Ventas del producto en la tienda en particular. Ésta es la variable objetivo a predecir.|

Al comenzar con el análisis del set de datos, en primera lugar se identificaron si existian datos faltantes.
Se descubre la presencia de datos nulos en el peso de alguno de los productos, y en el tamaño de algunas tiendas.

En el caso de los pesos faltantes, como contamos con el ID de los productos, simplemente se buscó el valor del peso de producto en aquellos registros del producto donde si estaba indicado el peso (como es el mismo producto, se ocupa el mismo peso para cada ID correspondiente)

A pesar de esto, quedaron cuatro (4) productos que no se pudo obtener el peso de esta forma, ya que fueron vendidos solamente en una tienda.
Estos productos fueron descartados del set de datos (aunque no es la opción más recomendable), ya que no teniamos alguna otra referencia para calcular este peso sin la asesoria de un experto en estos productos y además representaban un porcentaje muy ínfimo en las ventas totales de las tiendas (quizás eran productos fuera de producción en la actualidad o solo se vendieron una sola temporada)

