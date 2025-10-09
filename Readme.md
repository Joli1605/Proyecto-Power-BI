Proyecto Power BI

El objetivo de este proyecto fue crear un dashboard interactivo y dinámico que facilite la visualización y el análisis de datos sobre ventas, costos y rentabilidad.
El siguente informe describe las transformaciones clave aplicadas a los datos, las visualizaciones desarrolladas y las métricas definidas, con el propósito de mejorar la comprensión y el aprovechamiento de la información.
---

## Conexiones de Datos

Conexiones que se establecieron con las tablas de datos: 

- **BT_Orden_Detalle**
- **LK_Cliente**
- **LK_Metodo_De_Pago** 
- **LK_Vendedora**
- **LK_Producto**
- **LK_Proveedor**
- **LK_Locales_GEO**

---

 ## Transformaciones de Datos
Tabla LK_Vendedora
Separación del nombre completo: Se desglosó en las columnas "Nombre" y "Apellido".

Categorización de género: Se añadió la columna "Sexo" con valores "Femenino" o "Masculino".

Depuración de datos: Se eliminaron las columnas "Teléfono" y "Correo" por considerarse innecesarias.

Validación de integridad: Se aseguraron datos limpios y sin filas vacías.

Tabla LK_Cliente
Unificación del nombre: Se creó la columna "Nombre completo" combinando "Nombre" y "Apellido".

Depuración de datos: Se eliminaron las columnas originales "Nombre" y "Apellido".

Validación de integridad: Se garantizaron datos completos y sin inconsistencias.

Tabla LK_Metodo_De_Pago
Depuración de datos: Se eliminó la opción "Club card" de los métodos de pago.

Estandarización del formato: Todos los métodos de pago se convirtieron a mayúsculas.

Validación de integridad: Se verificó la ausencia de filas vacías.

Tabla LK_Producto
Ajuste de encabezados: Se estableció la primera fila como encabezado.

Reorganización de datos: Se movió la columna "Precio" al final para mejorar la disposición de la información.

Segmentación de precios: Se añadió la columna "Segmento" con las siguientes categorías:

Bronce: 1 a 30

Plata: 31 a 200

Oro: 201 a 2000 

Validación de integridad: Se garantizaron datos completos y sin errores.

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

#Conclusión
Este proyecto demuestra cómo Power BI simplifica la integración y el análisis de datos provenientes de diversas fuentes, asegurando su adecuada limpieza y organización. Las visualizaciones generadas ofrecen una visión precisa de las ventas, los costos y la rentabilidad, lo que permite tomar decisiones más informadas y estratégicas.
---

¿Tienes preguntas o sugerencias? ¡Contáctame!  
📧 **Correo:** jorgelinapramos@hotmail.com  
🌐 **LinkedIn:** [Jorgelina Ramos](https://www.linkedin.com/in/jorgelina-p-l-ramos-83564422b/)  
📞 **Teléfono:** +549 2396510483
