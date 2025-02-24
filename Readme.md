Proyecto Power BI

Este proyecto tuvo como objetivo desarrollar un dashboard interactivo y dinámico para mejorar la visualización y el análisis de datos sobre ventas, costos y rentabilidad.

El informe incluye las principales transformaciones de datos realizadas, las visualizaciones creadas y las métricas implementadas para facilitar una interpretación eficiente de la información.
---

## Conexiones de Datos

Se establecieron conexiones con las siguientes tablas de datos:

- **BT_Orden_Detalle**
- **LK_Cliente**
- **LK_Metodo_De_Pago**
- **LK_Vendedora**
- **LK_Producto**
- **LK_Proveedor**
- **LK_Locales_GEO**

---

## Transformaciones de Datos

### Tabla LK_Vendedora

1. **Separación del nombre completo:** Se dividió en las columnas "Nombre" y "Apellido".
2. **Categorización de género:** Se añadió la columna "Sexo", categorizando como "Femenino" o "Masculino".
3. **Eliminación de columnas innecesarias:** Se eliminaron "Teléfono" y "Correo".
4. **Integridad de datos:** Se garantizaron datos limpios y sin filas vacías.

### Tabla LK_Cliente

1. **Combinación de nombre y apellido:** Se creó la columna "Nombre completo".
2. **Eliminación de columnas innecesarias:** Se eliminaron "Nombre" y "Apellido".
3. **Integridad de datos:** Se validaron datos limpios y completos.

### Tabla LK_Metodo_De_Pago

1. **Eliminación de método de pago:** Se excluyó "Club card".
2. **Conversión a mayúsculas:** Todos los métodos de pago se escribieron en mayúsculas.
3. **Integridad de datos:** Validación sin filas vacías.

### Tabla LK_Producto

1. **Ajuste de encabezados:** La primera fila se configuró como encabezado.
2. **Reordenamiento de columnas:** La columna "Precio" se movió al final.
3. **Categorización de precios:** Se añadió la columna "Segmento" con categorías:
   - "Bronce" (1 a 30)
   - "Plata" (31 a 200)
   - "Oro" (201 a 2000).
4. **Integridad de datos:** Garantía de datos completos y sin errores.

---

## Relaciones Entre Tablas

Se configuraron relaciones entre las tablas de dimensiones (LK) y la tabla de hechos (BT_Orden_Detalle), asegurando consistencia y sin duplicados. Particularmente:

- **LK_Vendedora** y **BT_Orden_Detalle**
- **LK_Metodo_De_Pago** y **BT_Orden_Detalle**

---

## Columnas Calculadas en BT_Orden_Detalle

1. **Costo:** `Unidades vendidas * Costo unidad`
2. **Venta:** `Precio unidad * Unidades vendidas`
3. **Promoción:**
   - "En falta" si el valor es vacío.
   - "Sin promoción" si el valor es 0.
   - "Con promoción" si el valor es 3.

---

## Métricas en BT_Orden_Detalle

1. Total de Ventas ($)  
2. Total de Ventas del mes anterior ($)  
3. Total de Costos ($)  
4. Cantidad de Ventas  
5. Cantidad de Unidades Vendidas  
6. Rentabilidad ($)  
7. Venta Máxima  
8. Venta Mínima  

---

## Visualizaciones

### Página Overview

1. **Fondo personalizado:** Imagen "Fondo para tablero.jpg" con 20% de transparencia.  
2. **Visualizaciones clave:**
   - Tarjetas: Total de Ventas, Total de Costos, Rentabilidad, Unidades Vendidas.
   - Gráficos:
     - Evolutivo: Ventas y Rentabilidad por Año/Mes.
     - Barras agrupadas: Ventas por Método de Pago.
     - Costos por Categoría de Producto.

### Página Detalle de Ventas

1. **Segmentadores de datos:**
   - Fecha (rango)
   - Location
   - Métodos de pago
2. **Visualizaciones:**
   - Tarjetas: Total Ventas, Total Costo, Rentabilidad.
   - Tabla: Location, Categoría, Total Venta, Total Costo.
   - Treemap: Ventas por Producto (color: Rentabilidad, tamaño: Venta).

---

## Conclusión

Este proyecto demuestra el uso de Power BI para consolidar y analizar datos de múltiples fuentes, garantizando su limpieza y estructura. Las visualizaciones diseñadas ofrecen información clara sobre ventas, costos y rentabilidad, permitiendo una toma de decisiones estratégica y basada en datos.

---

¿Tienes preguntas o sugerencias? ¡Contáctame!  
📧 **Correo:** jorgelinapramos@hotmail.com  
🌐 **LinkedIn:** [Jorgelina Ramos](https://www.linkedin.com/in/jorgelina-p-l-ramos-83564422b/)  
📞 **Teléfono:** +549 2396510483
