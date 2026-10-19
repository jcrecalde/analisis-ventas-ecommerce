# Análisis de ventas de e-commerce

Proyecto de análisis exploratorio de ventas realizado con **Python, Pandas, Matplotlib y Power BI**.

Quise entender qué productos y categorías generan más ingresos, cómo cambian las ventas entre meses y qué ciudades aportan más facturación. Primero revisé la calidad de los datos y después calculé indicadores para compararlos desde distintas perspectivas.

## Datos utilizados

- **1.000 órdenes** y **7 columnas de entrada**.
- Período: **1 de enero al 29 de junio de 2026**.
- Archivo de entrada: `ecommerce_sales_1000_records.csv`.
- El dataset utilizado es de práctica. No representa una experiencia con una empresa real.
- El archivo original no identifica una moneda; los importes se muestran como unidades monetarias, aunque el diseño de Power BI use `$` como formato visual.

**Importante sobre el CSV:** el dataset no está incluido en el repositorio hasta verificar sus condiciones de redistribución. Para ejecutar el análisis hay que obtener el archivo de su fuente original y guardarlo con el nombre `ecommerce_sales_1000_records.csv` en la misma carpeta del notebook. El enlace exacto a la fuente está pendiente de documentar.

## Qué analicé

1. Calidad del dataset: nulos, duplicados, identificadores de órdenes, categorías y fechas.
2. Facturación por orden: `Revenue = Quantity × Price`.
3. Indicadores generales: facturación, órdenes, unidades y ticket promedio.
4. Productos y categorías: facturación, unidades, precio y participación.
5. Ciudades: ingresos, órdenes y ticket promedio.
6. Evolución mensual: comparaciones y variaciones frente al mes anterior.
7. Resúmenes exportados a Excel para el dashboard de Power BI.

## Algunos resultados

| Indicador | Resultado |
|---|---:|
| Facturación total | 27.620.651,09 |
| Órdenes | 1.000 |
| Unidades | 3.035 |
| Ticket promedio por orden | 27.620,65 |
| Participación de Electronics | 78,23 % |
| Producto con mayor facturación | Laptop: 11.411.335,18 |
| Producto con más unidades | T-Shirt: 259 |
| Variación junio vs. mayo | −21,55 % |

Electronics concentra gran parte de la facturación, pero esto por sí solo no determina qué decisiones conviene tomar. En el dashboard acompaño estos hallazgos con posibles líneas de análisis comercial.

## Cómo ejecutar el notebook

Con Python instalado:

```bash
python -m pip install -r requirements.txt
jupyter notebook analisis_ecommerce.ipynb
```

Antes de ejecutarlo, colocá el CSV de entrada junto al notebook. La última celda genera `ecommerce_analytics_outputs.xlsx` con los datos preparados y los resúmenes.

## Visualizaciones

El proyecto incluye un dashboard de Power BI con indicadores, filtros por mes, categoría, ciudad y producto, además de una página de hallazgos y recomendaciones. **Las capturas del dashboard y el archivo `.pbix` se incorporarán después de la revisión final.**

## Alcance y limitaciones

El dataset no incluye márgenes, costos, inventario, devoluciones, historial de campañas ni otros factores que permitirían explicar las variaciones de ventas. Las recomendaciones son posibilidades para investigar, no decisiones comerciales confirmadas.
