# Análisis estadístico y geoespacial de la rentabilidad agrícola en el municipio de La Paz, Cesar

**Autor:** Nedilson Pushaina Ramírez
**Universidad:** Universidad Nacional de Colombia – Sede de La Paz
**Programa:** Estadística
**Tipo de documento:** Trabajo de grado
**Año de análisis:** 2024

---

## Descripción general

Este repositorio contiene el desarrollo del trabajo de grado titulado **“Análisis estadístico y geoespacial de la rentabilidad agrícola en el municipio de La Paz, Cesar”**.

El proyecto fue desarrollado en **R y RStudio** mediante un archivo principal en formato **R Markdown**, donde se integran el procesamiento de bases de datos agrícolas, el cálculo de indicadores de rentabilidad, el análisis de precipitación, la estimación de modelos estadísticos y la elaboración de mapas temáticos interactivos.

El análisis se centra en los cultivos de **café, cacao y frijol**, debido a su importancia dentro de la base agrícola del municipio y a la disponibilidad de información productiva, económica y espacial.

---

## Objetivo general

Analizar la rentabilidad de los sistemas agrícolas del municipio de La Paz, Cesar, mediante el uso de herramientas estadísticas y geoespaciales.

---

## Objetivos específicos

1. Identificar y caracterizar los principales cultivos y sistemas agrícolas presentes en el municipio de La Paz, Cesar, recopilando información productiva, económica y espacial proveniente de fuentes institucionales y bases de datos públicas.

2. Analizar la relación entre variables agroambientales y productivas, evaluando cómo factores como precipitación, tipo de suelo y disponibilidad de recursos influyen en la productividad y rentabilidad agrícola.

3. Elaborar mapas temáticos y análisis espaciales que representen la distribución de los cultivos y los niveles de rentabilidad, identificando zonas críticas y áreas con potencial productivo.

---

## Funcionamiento del repositorio

Este repositorio está organizado para permitir la revisión y reproducción del análisis realizado en el trabajo de grado. El archivo principal es:

```text
trabajo-grado-rentabilidad-agricola.Rmd
```

Este archivo contiene el texto del documento, el código utilizado, las tablas, gráficos, modelos estadísticos y mapas interactivos.

Al ejecutar el archivo `.Rmd` en RStudio, se genera el documento final en formato HTML:

```text
trabajo-grado-rentabilidad-agricola.html
```

El archivo HTML permite visualizar el documento completo, incluyendo los mapas interactivos desarrollados con herramientas geoespaciales.

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
│   │   ├── POWER_Point_Daily_20240101_20241231_010d38N_073d17W_LST.csv
│   │   └── shapefiles/
│   │       ├── veredas_con_datos.dbf
│   │       ├── veredas_con_datos.prj
│   │       ├── veredas_con_datos.shp
│   │       └── veredas_con_datos.shx
│   │
│   └── processed/
│       └── precipitacion_mensual_LaPaz_2024.csv
│
├── trabajo-grado-rentabilidad-agricola.Rmd
├── trabajo-grado-rentabilidad-agricola.html
├── trabajo-grado-rentabilidad-agricola_files/
├── estilos.css
├── analisis agricola.Rproj
├── README.md
└── .gitignore
```

---

## Descripción de carpetas y archivos

| Elemento                                     | Descripción                                                                                  |
| -------------------------------------------- | -------------------------------------------------------------------------------------------- |
| `data/raw/`                                  | Contiene las bases de datos originales utilizadas en el análisis.                            |
| `data/raw/shapefiles/`                       | Contiene los archivos espaciales utilizados para los mapas por vereda.                       |
| `data/processed/`                            | Contiene bases procesadas o derivadas del análisis, como la precipitación mensual.           |
| `trabajo-grado-rentabilidad-agricola.Rmd`    | Archivo principal del proyecto. Contiene el documento y el código del análisis.              |
| `trabajo-grado-rentabilidad-agricola.html`   | Documento final generado a partir del R Markdown.                                            |
| `trabajo-grado-rentabilidad-agricola_files/` | Carpeta generada automáticamente por R Markdown para que el HTML funcione correctamente.     |
| `estilos.css`                                | Archivo de estilos utilizado para mejorar la presentación visual del documento HTML.         |
| `analisis agricola.Rproj`                    | Archivo del proyecto de RStudio. Se recomienda abrir este archivo para trabajar el proyecto. |
| `.gitignore`                                 | Archivo que indica qué elementos no deben ser incluidos en el repositorio.                   |

---

## Bases de datos utilizadas

El análisis utiliza las siguientes bases de datos:

### Bases agrícolas

```text
data/raw/corrver.xlsx
data/raw/productos_a.xlsx
data/raw/rend_productores_2024.csv
```

Estas bases contienen información relacionada con corregimientos, veredas, líneas productivas, productores, área sembrada, producción, precios, costos y cultivos.

### Datos climáticos

```text
data/raw/POWER_Point_Daily_20240101_20241231_010d38N_073d17W_LST.csv
```

Este archivo contiene datos diarios de precipitación para el año 2024, obtenidos de NASA POWER.

A partir de esta información se generó la base procesada:

```text
data/processed/precipitacion_mensual_LaPaz_2024.csv
```

### Información espacial

```text
data/raw/shapefiles/
```

Esta carpeta contiene el shapefile de veredas utilizado para la elaboración de mapas temáticos y análisis espacial.

---


---

## Análisis realizados

El proyecto incluye los siguientes análisis:

1. Caracterización de las líneas productivas agrícolas del municipio.
2. Selección de los cultivos de café, cacao y frijol.
3. Cálculo de producción, área sembrada, costos, ingresos, margen y ROI.
4. Análisis descriptivo mediante tablas, gráficos de barras, histogramas y boxplots.
5. Incorporación de la precipitación como variable agroambiental.
6. Estimación de un modelo de regresión lineal múltiple.
7. Elaboración de mapas interactivos por vereda.
8. Aplicación del Índice de Moran global para evaluar autocorrelación espacial.

---

---

## Requisitos para ejecutar el proyecto

Para ejecutar el proyecto se requiere tener instalado:

* R
* RStudio
* Git, si se desea clonar o actualizar el repositorio

También se utilizan los siguientes paquetes de R:

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

1. Descargar o clonar el repositorio.

2. Abrir el proyecto en RStudio desde el archivo:

```text
analisis agricola.Rproj
```

3. Abrir el archivo principal:

```text
trabajo-grado-rentabilidad-agricola.Rmd
```

4. Verificar que las bases de datos se encuentren dentro de las carpetas:

```text
data/raw/
data/processed/
```

5. Ejecutar el documento con la opción:

```text
Knit → Knit to HTML
```

6. El archivo final generado será:

```text
trabajo-grado-rentabilidad-agricola.html
```

---

## Visualización del documento HTML

El archivo HTML puede visualizarse correctamente descargando el repositorio y abriendo el archivo:

```text
trabajo-grado-rentabilidad-agricola.html
```

en un navegador web.

Debido a que GitHub no siempre permite visualizar directamente archivos HTML interactivos desde la vista del repositorio, especialmente cuando contienen mapas interactivos, se recomienda descargar el proyecto o utilizar GitHub Pages para su publicación como página web.

---

## Reproducibilidad

El proyecto utiliza rutas relativas, por ejemplo:

```text
data/raw/rend_productores_2024.csv
data/raw/shapefiles/veredas_con_datos.shp
data/processed/precipitacion_mensual_LaPaz_2024.csv
```

Esto permite que el análisis pueda ejecutarse en otro computador siempre que se conserve la estructura del repositorio.

---

## Consideraciones sobre los datos

Las bases de datos utilizadas no contienen información personal sensible de los productores. Los resultados se presentan de forma agregada por cultivo y por vereda, con fines académicos y de análisis estadístico.

---

## Estado del proyecto

El repositorio contiene el documento principal del trabajo de grado, las bases de datos utilizadas, los archivos espaciales, el archivo HTML generado y los estilos visuales empleados para su presentación.
