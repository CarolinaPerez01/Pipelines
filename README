**Transformación de Datos con Pipelines**

**Autor:** Carolina Pérez Molina

**Descripción**
Este proyecto tiene como objetivo la limpieza y transformación de datos utilizando sklearn.pipeline. Se trabaja con el conjunto de datos 'dirty_cafe_sales.csv', realizando un análisis exploratorio de datos (EDA), pues esto nos mostrará los errores que existen en el Dataframe, y luego según los errores encontrados se aplicaron transformaciones con pipelines.

**Datos**
El dataset "dirty_cafe_sales.csv" contiene 10,000 registros sobre ventas en una cafetería. Sin embargo, presenta problemas de calidad como valores faltantes, errores tipográficos y datos inconsistentes.

- **Transaction ID:** Identificador único de cada transacción.
- **Item:** Producto comprado (ej. café, pastel, galleta). 
- **Quantity:** Cantidad de unidades compradas de un producto.
- **Price Per Unit:** Precio unitario del producto.
- **Total Spent:** Precio total de la transacción.
- **Payment Method:** Método de pago usado (ej. tarjeta de crédito, efectivo, billetera digital).
- **Location:** Ubicación de la compra (ej. "In-store", "Takeaway").
- **Transaction Date:** Fecha de la compra.

**Proceso realizado**
- Se realizó un análisis exploratorio de datos (EDA) para observar los datos e identificar los errores que se corregirían con pipelines.
- En el EDA se identificó que todas las columnas fueron leídas como object, por lo que se modificaron a 'category' y 'float' para poder aplicar transformaciones con pipelines.
- Luego se realizaron trandormaciones con pipelines:
     - Para los valores faltantes en los datos numéricos, se imputaron utilizando el promedio de los demás valores.
     - No se cambió la escala de los números, ya que esto podría afectar la interpretación de los datos, dado que las variables numéricas corresponden a precios y cantidades.
     - Para las variables categóricas con datos faltantes, se imputó utilizando la moda.
     - Se aplicó la transformación 'One Hot Encoding', pero solo a los métodos de pago y la ubicación de la compra. No se utilizó en la variable 'Item' para evitar la generación de demasiadas columnas, lo que dificultaría la interpretación de los datos. Además, para evitar la trampa de las variables ficticias, se eliminó la primera columna generada, asumiendo que si una fila tiene 0, el 1 corresponde a la categoría faltante. En este caso, la categoría implícita para la ubicación es 'In-store' y para el método de pago es 'Cash'. 
     - Finalmente, se realizó una transformación en la fecha, dividiendo la columna en día, mes y año.

**Concluisones**
- La transformación de variables categóricas permitió estandarizar los datos y facilitar su uso en análisis futuros sin generar un exceso de columnas innecesarias.
- La estrategia de imputación de valores faltantes con la moda y el promedio garantizó que no se perdiera información relevante en el dataset.
- No escalar los datos numéricos fue una decisión acertada, ya que al tratarse de precios y cantidades, conservar su magnitud original permite una mejor interpretación.
- La transformación de fechas en día, mes y año facilita su uso en análisis temporales y permite extraer patrones estacionales en las ventas.
- El uso de pipelines optimizó el proceso de limpieza y transformación, haciendo que el preprocesamiento sea más eficiente y reproducible para futuros datasets.