# Análisis estadístico y geoespacial de la rentabilidad agrícola en La Paz, Cesar

## Descripción del proyecto

Este repositorio contiene el trabajo de grado titulado **“Análisis estadístico y geoespacial de la rentabilidad agrícola en el municipio de La Paz, Cesar”**.

El objetivo principal del proyecto es analizar la rentabilidad de los sistemas agrícolas del municipio de La Paz, Cesar, mediante el uso de herramientas estadísticas y geoespaciales. El análisis se centra en los cultivos de **café, cacao y frijol**, debido a su importancia dentro de la base de datos agrícola y a la disponibilidad de información productiva, económica y espacial.

El trabajo fue desarrollado en **R y RStudio**, utilizando información agrícola correspondiente al año 2024, datos de precipitación obtenidos de NASA POWER y herramientas de análisis estadístico y espacial.

---

## Objetivo general

Analizar la rentabilidad de los sistemas agrícolas del municipio de La Paz, Cesar, mediante el uso de herramientas estadísticas y geoespaciales.

---

## Objetivos específicos

1. Identificar y caracterizar los principales cultivos y sistemas agrícolas presentes en el municipio de La Paz, Cesar, recopilando información productiva, económica y espacial proveniente de fuentes institucionales y bases de datos públicas.

2. Analizar la relación entre variables agroambientales, productivas y económicas, evaluando cómo factores como la precipitación, el área sembrada, la producción, los precios y los costos influyen en la productividad y rentabilidad agrícola.

3. Elaborar mapas temáticos y análisis espaciales que representen la distribución de los cultivos y los niveles de rentabilidad, identificando zonas críticas y áreas con potencial productivo.

---

## Estructura del repositorio

```text
analisis-agricola/
│
├── data/
│   ├── raw/
│   │   ├── corrver.xlsx
│   │   ├── productos_a.xlsx
│   │   ├── rend_productores_2024.csv
│   │   └── POWER_Point_Daily_20240101_20241231_010d38N_073d17W_LST.csv
│   │
│   └── processed/
│       └── precipitacion_mensual_LaPaz_2024.csv
│
├── trabajo-grado-rentabilidad-agricola.Rmd
├── trabajo-grado-rentabilidad-agricola.html
├── estilos.css
├── analisis agricola.Rproj
├── README.md
└── .gitignore
```

---

## Descripción de los archivos principales

| Archivo o carpeta                          | Descripción                                                                                                                                        |
| ------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------- |
| `trabajo-grado-rentabilidad-agricola.Rmd`  | Documento principal del trabajo de grado en formato R Markdown. Contiene el código, análisis, resultados, gráficos, mapas y redacción del informe. |
| `trabajo-grado-rentabilidad-agricola.html` | Versión final generada en HTML. Permite visualizar el documento con tablas, gráficos y mapas interactivos.                                         |
| `estilos.css`                              | Archivo de estilos utilizado para mejorar la presentación visual del documento HTML.                                                               |
| `data/raw/`                                | Carpeta que contiene las bases de datos originales utilizadas en el análisis.                                                                      |
| `data/processed/`                          | Carpeta que contiene bases de datos procesadas o transformadas durante el análisis.                                                                |
| `analisis agricola.Rproj`                  | Proyecto de RStudio para abrir el repositorio de forma organizada.                                                                                 |
| `.gitignore`                               | Archivo que indica qué elementos no deben ser subidos al repositorio.                                                                              |

---

## Fuentes de información

Las principales fuentes de información utilizadas fueron:

* **Oficina de UMATA, Control Ambiental y Gestión del Riesgo del municipio de La Paz, Cesar**: base de datos agrícola con información productiva, económica y espacial de productores del municipio.
* **Productores agrícolas locales**: información utilizada para la estimación de costos de producción por hectárea.
* **NASA POWER**: datos de precipitación corregida para el año 2024.
* **OpenStreetMap**: mapa base utilizado en la visualización geoespacial interactiva.
* **R y paquetes especializados**: herramientas utilizadas para el análisis estadístico, gráfico y espacial.

---

## Variables utilizadas

Las principales variables consideradas en el análisis fueron:

| Variable           | Descripción                                                           |
| ------------------ | --------------------------------------------------------------------- |
| `VEREDA`           | Vereda donde se ubica la unidad productiva.                           |
| `CULTIVO`          | Tipo de cultivo analizado: café, cacao o frijol.                      |
| `AREA_HA`          | Área sembrada en hectáreas.                                           |
| `PRODUCCION_KG`    | Producción agrícola en kilogramos.                                    |
| `PRECIO_KG`        | Precio de venta por kilogramo.                                        |
| `COSTO_HA`         | Costo de producción por hectárea.                                     |
| `INGRESO_BRUTO`    | Ingreso obtenido por la producción vendida.                           |
| `COSTO_TOTAL`      | Costo total estimado de producción.                                   |
| `MARGEN`           | Diferencia entre ingreso bruto y costo total.                         |
| `ROI`              | Retorno sobre la inversión, utilizado como indicador de rentabilidad. |
| `PRECIPITACION_MM` | Precipitación acumulada asociada al cultivo.                          |

---

## Indicadores calculados

El análisis económico se desarrolló a partir de los siguientes indicadores:

### Ingreso bruto

```text
Ingreso Bruto = Producción (kg) × Precio ($/kg)
```

### Costo total

```text
Costo Total = Área sembrada (ha) × Costo por hectárea
```

### Margen de ganancia

```text
Margen = Ingreso Bruto - Costo Total
```

### Retorno sobre la inversión

```text
ROI = (Ingreso Bruto - Costo Total) / Costo Total
```

El ROI fue utilizado como indicador principal de rentabilidad agrícola.

---

## Metodología general

El proyecto se desarrolló en las siguientes etapas:

1. **Recolección y organización de datos**
   Se utilizaron bases de datos agrícolas del municipio de La Paz, Cesar, junto con información de precipitación obtenida de NASA POWER.

2. **Depuración y construcción de variables**
   Se organizaron las variables productivas y económicas, y se calcularon indicadores como ingreso bruto, costo total, margen y ROI.

3. **Análisis descriptivo**
   Se caracterizaron los cultivos analizados mediante tablas, gráficos de barras, histogramas y boxplots.

4. **Análisis agroambiental**
   Se incorporó la precipitación como variable climática para evaluar su relación con la rentabilidad agrícola.

5. **Modelo de regresión múltiple**
   Se estimó un modelo de regresión lineal múltiple para analizar la relación entre el ROI y variables como precipitación, área sembrada, producción, precio y costo.

6. **Análisis geoespacial**
   Se elaboraron mapas temáticos por vereda para representar productores, cultivo predominante, producción, área agrícola y rentabilidad.

7. **Índice de Moran**
   Se aplicó el Índice de Moran global para evaluar la presencia de autocorrelación espacial en la rentabilidad promedio por vereda.

---

## Modelo estadístico utilizado

El modelo de regresión múltiple utilizado fue:

```text
ROI_i = β0 + β1 Precipitación_i + β2 Área_i + β3 Producción_i + β4 Precio_i + β5 Costo_i + ε_i
```

Donde:

* `ROI_i`: rentabilidad del productor `i`.
* `Precipitación_i`: precipitación acumulada asociada al cultivo.
* `Área_i`: área sembrada en hectáreas.
* `Producción_i`: producción en kilogramos.
* `Precio_i`: precio por kilogramo.
* `Costo_i`: costo por hectárea.
* `ε_i`: término de error del modelo.

---

## Principales resultados

Los resultados más relevantes del análisis fueron:

* El **café** fue el cultivo con mayor número de productores, mayor área sembrada y mayor producción total.
* El **cacao** presentó los mayores niveles promedio de rentabilidad medidos mediante el ROI.
* La producción y el precio por kilogramo tuvieron una relación positiva con la rentabilidad.
* El área sembrada y el costo por hectárea presentaron una relación negativa con el ROI en el modelo estimado.
* La precipitación presentó un efecto positivo, aunque no estadísticamente significativo.
* El modelo de regresión múltiple explicó aproximadamente el 51% de la variación del ROI.
* El Índice de Moran indicó que no existe autocorrelación espacial significativa en la rentabilidad agrícola entre las veredas analizadas.

---

## Requisitos para ejecutar el proyecto

Para ejecutar el proyecto se requiere tener instalado:

* R
* RStudio
* Git, si se desea clonar o actualizar el repositorio

Además, se utilizan los siguientes paquetes de R:

```r
install.packages(c(
  "readxl",
  "dplyr",
  "ggplot2",
  "sf",
  "leaflet",
  "spdep",
  "knitr",
  "rmarkdown"
))
```

---

## Cómo ejecutar el proyecto

1. Descargar o clonar este repositorio.

2. Abrir el archivo del proyecto en RStudio:

```text
analisis agricola.Rproj
```

3. Abrir el archivo principal:

```text
trabajo-grado-rentabilidad-agricola.Rmd
```

4. Verificar que las bases de datos estén ubicadas en la carpeta:

```text
data/raw/
```

5. Ejecutar el documento haciendo clic en:

```text
Knit → Knit to HTML
```

6. El resultado final se generará en el archivo:

```text
trabajo-grado-rentabilidad-agricola.html
```

---

## Organización de datos

Los datos se organizaron en dos carpetas:

* `data/raw/`: contiene los archivos originales utilizados en el análisis.
* `data/processed/`: contiene archivos procesados o derivados, como la precipitación mensual.

Esta organización permite mejorar la reproducibilidad del proyecto y facilita que otros usuarios puedan revisar el flujo de trabajo.

---

## Consideraciones éticas y de uso de datos

Las bases de datos utilizadas no contienen información personal sensible de los productores. El análisis se realizó con fines académicos y los resultados se presentan de forma agregada, principalmente por cultivo y por vereda.

---

## Autor

**Nedilson Pushaina Ramírez**
Universidad Nacional de Colombia
Sede de La Paz
Trabajo de grado – Estadística
2026
