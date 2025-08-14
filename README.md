# proyecto_4_limpieza_informe
# Limpiar datos y preparar informe | Hábitos de compra de los clientes de Instacart | Data WranglingGitHub

## Descripción del Proyecto
Análisis de datos de un conjunto modificado de Instacart (plataforma de entrega de comestibles)
Con el objetivo de evaluar y mejorar la calidad de los datos para análisis exploratorio. El trabajo se centró en:

- Limpieza de datos
- Transformación y estandarización
- Manejo de valores ausentes y duplicados
- Preparación para análisis avanzado

## Objetivos del Análisis

✅ Identificar y corregir problemas de calidad de datos  
✅ Estandarizar tipos de datos para análisis preciso  
✅ Descubrir patrones en hábitos de compra  
✅ Visualizar distribución temporal de pedidos  
✅ Analizar tasa de reordenación como indicador de fidelidad  

## Tecnologías Utilizadas

| Categoría | Herramientas |
|-----------|-------------|
| Lenguaje | Python |
| Bibliotecas | Pandas, NumPy |
| Visualización | Matplotlib, Seaborn |
| Métodos clave | `isna()`, `duplicated()`, `fillna()`, `astype()`, `value_counts()`, `merge()` 

## Pasos Clave del Análisis

### 1. Carga y Evaluación de la Calidad de los Datos
📂 Carga y Evaluación de la Calidad de los Datos: 
Se cargan los 5 archivos CSV (instacart_orders, products, order_products, aisles, departments)
Se realizó una inspección inicial para identificar valores ausentes, duplicados y tipos de datos incorrectos.

🔍 Inspección inicial para identificar:
- Valores ausentes (NaN)
- Registros duplicados
- Tipos de datos incorrectos
- Inconsistencias en formatos

### 2. Limpieza y Normalización

#### Manejo de Valores Ausentes
| Columna | Tratamiento | Acción |
|---------|-------------|--------|
| `days_since_prior_order` | NaN → 0.0 | Relleno con valor por defecto |
| `product_name` | NaN → 'unknown' | Marcador para valores faltantes |
| `add_to_cart_order` | NaN → 999 | Conversión a tipo entero |

Se identificaron y gestionaron los valores ausentes en las tablas:
- Los NaN en days_since_prior_order se reemplazaron con 0.0
- Los de product_name se sustituyeron por 'unknown'
- Los de add_to_cart_order por 999, para luego convertir la columna a tipo entero.
  
Se verificaron y eliminaron los duplicados que pudieran existir, tanto en filas completas como en combinaciones de columnas clave.


### 3. Análisis Exploratorio y Visualización:

- Se verificó que los valores en las columnas order_hour_of_day y order_dow fueran razonables, oscilando entre 0-23 y 0-6 respectivamente.
- Se generaron gráficos de barras para mostrar la frecuencia de pedidos por hora del día y por día de la semana.
- Se creó un histograma para visualizar la distribución de los días transcurridos entre pedidos.
- Se examinó la proporción de productos reordenados para comprender la lealtad del cliente.

### Conclusiones
Este proyecto demostró un manejo sólido de las técnicas de limpieza y preparación de datos en Python.
La información procesada reveló patrones de compra significativos, como la preferencia por las mañanas y los fines de semana para hacer pedidos.
Además, el análisis de productos reordenados y la frecuencia de compra resalta la fidelidad de los clientes de Instacart.
Estos hallazgos son valiosos para cualquier estrategia de negocio que busque optimizar la operación y el marketing.
