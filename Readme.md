
# Proyecto de Power BI

El objetivo de este proyecto fue crear un dashboard interactivo y dinámico que permitiera una visualización y análisis eficiente de datos relacionados con ventas, costos y rentabilidad. En su desarrollo, se destacaron las principales transformaciones aplicadas a cada conjunto de datos y las visualizaciones diseñadas para optimizar el proceso de análisis.

## Conexiones de Datos
Conexiones a las siguientes tablas:

- BT_Orden_Detalle
- LK_Cliente
- LK_Metodo_De_Pago
- LK_Vendedora
- LK_Producto
- LK_Proveedor
- LK_Locales_GEO

## Transformaciones de Datos

### Tabla LK_Vendedor

 Tabla LK_Vendedor, se ejecutaron varias transformaciones para limpiar y estructurar los datos:

1. **Separación del nombre completo:** Se dividió en dos columnas el nombre completo: "Nombre" y "Apellido".
2. **Categorización de género:** Se creó una columna condicional llamada "Sexo" para categorizar la columna "género" como "Femenino" cuando el género es "F" y "Masculino" cuando es "M".
3. **Eliminación de columnas innecesarias:** Se eliminaron las columnas "Teléfono" y "Correo".
4. **Integridad de datos:** Se garantizó que no existieran filas completamente vacías.

### Tabla LK_Cliente

Tabla LK_Cliente, se realizaron las siguientes transformaciones:

1. **Combinación de nombre y apellido:** Se creó una columna "Nombre completo" combinando las columnas "Nombre" y "Apellido", separadas por una coma.
2. **Eliminación de columnas innecesarias:** Se eliminaron las columnas "Nombre" y "Apellido".
3. **Integridad de datos:** Se garantizó que no existieran filas completamente vacías.

### Tabla LK_Metodo_De_Pago

Transformaciones en la tabla LK_Metodo_De_Pago:

1. **Eliminación de método de pago:** Se eliminó el método de pago "Club card".
2. **Conversión a mayúsculas:** Todos los métodos de pago se convirtieron a mayúsculas.
3. **Integridad de datos:** Se garantizó que no existieran filas completamente vacías.

### Tabla LK_Producto

Para la tabla LK_Producto, se aplicaron las siguientes transformaciones:

1. **Ajuste de encabezados:** La primera fila se estableció como encabezado.
2. **Reordenamiento de columnas:** Las columnas se reordenaron para que "Precio" quedara al final.
3. **Categorización de precios:** Se creó una columna condicional llamada "Segmento" para categorizar la columna "Precio" en "Bronce" (1 a 30), "Plata" (31 a 200) y "Oro" (201 a 2000).
4. **Integridad de datos:** Se garantizó que no existieran filas completamente vacías.

## Relaciones Entre Tablas

Se establecieron las relaciones entre las tablas de dimensiones (LK) y la tabla de hechos (BT_Orden_Detalle), asegurando la correcta vinculación de los datos. Durante este proceso, se verificó que los campos relacionados no presentaran nombres duplicados en ambas tablas. En caso de detectar duplicados, se procedió a renombrarlos de manera adecuada para evitar conflictos. En particular, se prestó especial atención a las relaciones entre LK_Vendedor y BT_Orden_Detalle, así como entre LK_Metodo_De_Pago y BT_Orden_Detalle, garantizando la consistencia y la integridad de los datos.

## Columnas Calculadas en BT_Orden_Detalle

Se crearon las siguientes columnas calculadas en la tabla BT_Orden_Detalle:

1. **Costo:** Calculado como `Unidades vendidas * Costo unidad`.
2. **Venta:** Calculado como `Precio de unidad * Unidades vendidas`.
3. **Promoción:** Una columna con las siguientes categorías:
   - "En falta" si el valor es Blank (vacío)
   - "Sin promoción" si el valor es 0
   - "Con promoción" si el valor es 3

## Métricas en BT_Orden_Detalle

Las métricas creadas en la tabla BT_Orden_Detalle incluyen:

1. **Total de Ventas en $:** Utilizando la función SUM.
2. **Total de Ventas del mes anterior en $.**
3. **Total de Costos en $:** Utilizando la función SUM.
4. **Cantidad de Ventas:** Utilizando las funciones COUNT o COUNTROWS.
5. **Cantidad de Unidades Vendidas:** Utilizando la función SUM.
6. **Rentabilidad en $.**
7. **Venta Máxima.**
8. **Venta Mínima.**

## Página Overview

En la página Overview del dashboard, se realizaron las siguientes configuraciones y visualizaciones:

1. **Fondo del lienzo:** Se añadió el fondo "Fondo para tablero.jpg" con una transparencia del 20%.
2. **Visualizaciones de tarjetas:** Se crearon tarjetas para mostrar las siguientes medidas:
   - Total de Ventas
   - Total de Costos
   - Rentabilidad
   - Cantidad de Unidades Vendidas
3. **Gráfico evolutivo:** Se mostró el Total de Ventas y la Rentabilidad desglosados por Año y Mes.
4. **Gráfico de Columnas Agrupadas:** Se mostró el Total de Ventas desglosado por la descripción de los métodos de pago.
5. **Gráfico de Costos:** Se mostró el Total de Costos desglosado por la categoría del producto.

## Página Detalle de Ventas

En la página Detalle de Ventas, se incluyeron las siguientes visualizaciones y segmentadores de datos:

1. **Segmentadores de datos:** Se generaron segmentadores para:
   - Fecha (permitiendo seleccionar un rango de fechas "Entre")
   - Location (Lista desplegable)
   - Medios de pago (Lista desplegable)
2. **Visualizaciones en tarjetas:** Se mostraron las medidas Total Ventas, Total Costo y Rentabilidad.
3. **Tabla de datos:** Se incluyó una tabla que muestra "Location", "Categoría", "Total venta" y "Total costo".
4. **Gráfico de Treemap:** Se visualizó las ventas por jerarquías de productos (Categoría, Subcategoría y Producto), con el color representando la Rentabilidad y el tamaño representando la Venta.

Esta guía detalla las transformaciones de datos y las visualizaciones desarrolladas en el proyecto de Power BI, garantizando que los datos se encuentren limpios, estructurados y listos para un análisis exhaustivo.

**Conclusión**
En este proyecto, llevé a cabo la transformación y consolidación de datos provenientes de múltiples fuentes para desarrollar un dashboard interactivo y altamente funcional. Las transformaciones aplicadas aseguraron la consistencia y precisión de los datos, lo que facilitó un análisis confiable y eficiente.

Las visualizaciones generadas, incluyendo tarjetas de métricas, gráficos de evolución y treemaps, ofrecen una perspectiva clara y comprensible sobre aspectos clave como ventas, costos y rentabilidad. Además, la incorporación de segmentadores de datos permite a los usuarios interactuar con la información y filtrarla según criterios específicos, adaptándose a sus necesidades particulares.

El resultado es una herramienta robusta para la toma de decisiones estratégicas, que presenta datos limpios y organizados, ideales para un análisis detallado y adaptable del rendimiento del negocio.

¿Tienes alguna pregunta o sugerencia?
¡No dudes en contactarme!

Correo eléctronico: jorgelinapramos@hotmail.com

Linkedin: https://www.linkedin.com/in/jorgelina-p-l-ramos-83564422b/

Tel: +549 2396510483