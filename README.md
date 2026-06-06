# Análisis agrícola en La Paz, Cesar

Este repositorio contiene el código, las bases de datos y el documento HTML del trabajo de grado titulado:

**Análisis estadístico y geoespacial de la rentabilidad agrícola en el municipio de La Paz, Cesar**

El proyecto fue desarrollado en **R y RStudio** mediante un archivo principal en formato **R Markdown**. El análisis incluye procesamiento de bases agrícolas, cálculo de indicadores de rentabilidad, análisis de precipitación, modelos estadísticos y mapas interactivos.

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

## Archivos principales

| Archivo o carpeta                            | Descripción                                                                                                            |
| -------------------------------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| `trabajo-grado-rentabilidad-agricola.Rmd`    | Archivo principal del proyecto. Contiene el código, texto, gráficos, tablas, mapas y análisis.                         |
| `trabajo-grado-rentabilidad-agricola.html`   | Documento final generado a partir del R Markdown. Incluye los resultados y mapas interactivos.                         |
| `trabajo-grado-rentabilidad-agricola_files/` | Carpeta generada automáticamente por R Markdown. Contiene archivos necesarios para que el HTML funcione correctamente. |
| `estilos.css`                                | Archivo de estilos para mejorar la presentación visual del documento HTML.                                             |
| `data/raw/`                                  | Carpeta con las bases de datos originales utilizadas en el análisis.                                                   |
| `data/processed/`                            | Carpeta con bases procesadas o transformadas durante el análisis.                                                      |
| `analisis agricola.Rproj`                    | Archivo del proyecto de RStudio. Se recomienda abrir este archivo antes de ejecutar el análisis.                       |

---

## Bases de datos utilizadas

Las bases de datos se encuentran organizadas dentro de la carpeta `data/`.

### Datos originales

La carpeta `data/raw/` contiene las bases originales utilizadas en el análisis:

* `corrver.xlsx`: información relacionada con corregimientos y veredas.
* `productos_a.xlsx`: información de líneas productivas agrícolas.
* `rend_productores_2024.csv`: base principal con información productiva y económica de los productores.
* `POWER_Point_Daily_20240101_20241231_010d38N_073d17W_LST.csv`: datos diarios de precipitación obtenidos de NASA POWER.
* `shapefiles/`: archivos espaciales utilizados para la elaboración de mapas por vereda.

### Datos procesados

La carpeta `data/processed/` contiene archivos derivados del procesamiento de datos:

* `precipitacion_mensual_LaPaz_2024.csv`: precipitación mensual calculada a partir de los datos diarios de NASA POWER.

---

## Cómo ejecutar el proyecto

Para reproducir el análisis, se recomienda seguir estos pasos:

1. Descargar o clonar este repositorio.

2. Abrir el proyecto en RStudio desde el archivo:

```text
analisis agricola.Rproj
```

3. Abrir el archivo principal:

```text
trabajo-grado-rentabilidad-agricola.Rmd
```

4. Verificar que las bases de datos se encuentren en las carpetas:

```text
data/raw/
data/processed/
```

5. Instalar los paquetes necesarios de R, si no están instalados:

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

6. Ejecutar el documento usando:

```text
Knit → Knit to HTML
```

7. El resultado se generará en el archivo:

```text
trabajo-grado-rentabilidad-agricola.html
```

---

## Salida principal del proyecto

La salida principal es el documento HTML:

```text
trabajo-grado-rentabilidad-agricola.html
```

Este archivo contiene:

* resumen del trabajo;
* metodología;
* resultados descriptivos;
* cálculo de rentabilidad agrícola;
* modelo de regresión;
* mapas interactivos por vereda;
* análisis del Índice de Moran;
* conclusiones y referencias.

---

## Visualización del HTML

El archivo HTML puede abrirse localmente en el navegador después de descargar el repositorio.

Debido a que GitHub no siempre muestra archivos HTML interactivos directamente desde la vista del repositorio, para visualizarlo correctamente se recomienda:

1. Descargar el repositorio y abrir el archivo `.html` en el navegador; o
2. Publicar el documento mediante GitHub Pages.

---

## Notas sobre reproducibilidad

El proyecto utiliza rutas relativas, por ejemplo:

```r
data/raw/rend_productores_2024.csv
data/processed/precipitacion_mensual_LaPaz_2024.csv
```

Esto permite que el análisis pueda ejecutarse en otro computador siempre que se mantenga la estructura de carpetas del repositorio.

---

## Autor

**Nedilson Pushaina Ramírez**
Universidad Nacional de Colombia
Sede de La Paz
Trabajo de grado – Estadística
2026
