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

Se comienza con un análisis del dataset para tratar los valores nulos presentes.

Una vez concluida esto, se procede con un análisis exploratorio, donde se puede identificar cual es la tienda que más vende, que tipo de productos son los que más se han vendido en general en todas las tiendas, la distribución de alguna de las variables y la presencia de outliers, además de ver la matríz de correlación para ver que tan lineal es la relación entre las variables con la variable objetivo **Item_Outlet_Sales**

Finalmente, se procede a aplicar LabelEncoder para trabajar las características de tipo categóricas como tipo numéricas y luego se escalan los datos, mediante StandardScaler y dividimos el set de datos en Entrenamiento y Testeo.

Se prueban 3 tipos de modelos de regresión:

- Regresión Lineal.
- KNN Regresor
- Random Forest Regresor

Para estos tres modelos, obtenemos los puntajes R2 y la raíz del error cuadrático medio.
En base a estos puntajes, se opta por aquel modelo que presenta el R2 mayor y el menor error, que en este caso fue Random Forest Regressor.

Como conclusión, creo que se puede mejorar el modelo, realizando un análisis junto a alguien entendido en este tipo de industria, para revisar si todas las características del dataset son necesarias, ya que quizas reduciendo algunas se pueda mejorar alguno de los modelos presentados
