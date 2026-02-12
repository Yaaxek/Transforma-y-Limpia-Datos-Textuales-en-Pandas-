# Proyecto FastDelivery

## 1. Introducción
La empresa FastDelivery, un servicio de entrega de alimentos, ha estado gestionando su base de datos de clientes y pedidos en una hoja de cálculo de Excel. Dada la creciente cantidad de datos, se ha requerido manipular y optimizar esta información para facilitar futuros análisis.

## 2. Origen de los Datos
Los datos iniciales provienen de un archivo Excel llamado `banco_clientes.xlsx`.

## 3. Limpieza y Transformación de Datos Realizada
Se han llevado a cabo las siguientes operaciones para limpiar y estructurar los datos:

*   **Carga de Datos:** El archivo `banco_clientes.xlsx` fue cargado en un DataFrame de pandas para su manipulación.
*   **Normalización de Nombres:** La columna `nombre` (nombres de los clientes) fue convertida a mayúsculas para estandarizar el formato.
*   **Limpieza de Teléfonos:** Se eliminaron los paréntesis `()` de la columna `telefono` para uniformar el formato de los números.
*   **Extracción de Códigos Postales (CP):** Se creó una nueva columna `CP` extrayendo los códigos postales del formato `XXXXX-XXX` de la columna `direccion`.
*   **Separación de Dirección:** La columna `direccion` fue dividida en dos nuevas columnas: `Calle` y `Numero`, para una mejor granularidad de la información de ubicación.
*   **Eliminación de Columna Original:** La columna `direccion` original fue eliminada del DataFrame, ya que su información ahora está estructurada en `Calle`, `Numero` y `CP`.

## 4. Estado Actual del DataFrame `df`
El DataFrame `df` ahora contiene las siguientes columnas limpias y estructuradas:
*   `nombre`: Nombre del cliente en mayúsculas.
*   `telefono`: Número de teléfono sin paréntesis.
*   `CP`: Código postal del cliente.
*   `Calle`: Nombre de la calle de la dirección.
*   `Numero`: Número de la dirección.

## 5. Próximos Pasos Sugeridos
Con los datos ya limpios y estructurados, se pueden considerar los siguientes análisis y mejoras:

*   **Análisis Geográfico:** Utilizar los códigos postales y direcciones para mapear la distribución de clientes y optimizar rutas de entrega.
*   **Segmentación de Clientes:** Aplicar técnicas de agrupamiento para identificar diferentes segmentos de clientes basados en patrones de pedidos, ubicación, etc.
*   **Integración con Datos de Pedidos:** Si se cuenta con una base de datos de pedidos, unir esta información con los datos de clientes para analizar comportamientos de compra, frecuencia de pedidos, etc.
*   **Validación de Datos:** Implementar validaciones adicionales para asegurar la coherencia de los números de teléfono y códigos postales.
*   **Visualización de Datos:** Crear visualizaciones interactivas para explorar la base de clientes y sus características.
