# EDA: Tiempo en Pantallas, Sueño y Salud Mental en Adolescentes

Análisis Exploratorio de Datos (EDA) sobre cómo el tiempo frente a pantallas y los patrones de sueño afectan la salud mental de los adolescentes. Este proyecto está desarrollado en **R** y **R Markdown** con formato **Bookdown**.

---

##  Dataset

El conjunto de datos utilizado es **`screen_time_mental_health.csv`**, que contiene información sobre:

| Variable | Descripción | Tipo |
|----------|-------------|------|
| `subject_id` | Identificador único del participante | Numérico |
| `sex` | Sexo del participante (Boy/Girl) | Categórico |
| `screen_time_index` | Índice de tiempo total en pantallas | Numérico |
| `est_leisure_screen_hours` | Horas estimadas de pantalla en ocio | Numérico |
| `sleep_quality_index` | Índice de calidad del sueño | Numérico |
| `avg_sleep_hours` | Horas promedio de sueño | Numérico |
| `midsleep_weekend_hours` | Punto medio del sueño en fin de semana | Numérico |
| `social_jetlag_hours` | Desfase entre sueño de días hábiles y fines de semana | Numérico |
| `bdi_total` | Puntaje total en el Inventario de Depresión de Beck (BDI) | Numérico |
| `depressed` | Clasificación de depresión (0: No deprimido, 1: Deprimido) | Categórico |

> **Nota:** El dataset no contiene valores faltantes ni registros duplicados por `subject_id`.

---

## Requisitos

Para ejecutar este proyecto necesitas:

### Software
- **R** (versión ≥ 4.0.0) — [Descargar](https://cran.r-project.org/)
- **RStudio** (versión ≥ 2022.07) — [Descargar](https://posit.co/download/rstudio-desktop/)

### Paquetes de R
Instala los paquetes necesarios ejecutando:

```r
install.packages(c(
  "tidyverse",      # Manipulación y visualización de datos
  "knitr",          # Generación de reportes
  "kableExtra",     # Tablas profesionales
  "bookdown",       # Formato de libro
  "ggcorrplot",     # Matriz de correlación
  "gridExtra",      # Múltiples gráficos
  "scales",         # Formato de escalas
  "moments",        # Asimetría y curtosis
  "nortest",        # Pruebas de normalidad
  "DT"              # Tablas interactivas (opcional)
))
```

---

## Cómo abrir el proyecto desde GitHub hasta R

Sigue estos pasos para clonar y ejecutar el proyecto en tu máquina local:

### 1. Clonar el repositorio desde GitHub

**Opción A: Desde RStudio (recomendado)**

1. Abre RStudio
2. Ve a `File` → `New Project` → `Version Control` → `Git`
3. Pega la URL del repositorio:
   ```
   https://github.com/sjimenezurrea-sudo/ebook_Dataviz2026.git
   ```
4. Elige la carpeta donde quieres guardar el proyecto
5. Click en **Create Project**

**Opción B: Desde la terminal**

```bash
git clone https://github.com/sjimenezurrea-sudo/ebook_Dataviz2026.git
cd ebook_Dataviz2026
```

### 2. Abrir el proyecto en RStudio

1. Abre RStudio
2. Ve a `File` → `Open Project`
3. Selecciona el archivo **`ebook_Dataviz2026.Rproj`** dentro de la carpeta clonada
4. RStudio cargará automáticamente el entorno del proyecto

### 3. Verificar que el dataset esté en la carpeta

El archivo `screen_time_mental_health.csv` debe estar en la **raíz del proyecto**. Si no está, descárgalo y colócalo allí.

### 4. Compilar el libro (Bookdown)

En la consola de R, ejecuta:

```r
# Opción 1: Compilar todo el libro
bookdown::render_book("index.Rmd", "bookdown::gitbook")

# Opción 2: Compilar solo un capítulo (para probar)
bookdown::preview_chapter("01-eda.Rmd")
```

El libro compilado se generará en la carpeta **`_book/`** y podrás abrirlo en tu navegador.

### 5. Ver el libro en el navegador

Abre el archivo:
```
_book/index.html
```

---

## Estructura del Análisis (Bookdown)

El libro sigue la siguiente estructura de capítulos:

1. **Comprender el contexto** — Pregunta de investigación y variables
2. **Carga de librerías** — Paquetes necesarios
3. **Importación de datos** — Carga del dataset
4. **Limpieza y preparación** — Tipos de datos, valores faltantes, outliers
5. **Análisis univariado** — Distribuciones, variable objetivo, categóricas
6. **Análisis bivariado** — Correlaciones, selección de variables, interacciones
7. **Documentación de hallazgos** — Conclusiones y recomendaciones

---

##  Tecnologías Utilizadas

- **R** — Lenguaje de programación estadística
- **R Markdown** — Documentos dinámicos
- **Bookdown** — Libros y documentación técnica
- **tidyverse** — Colección de paquetes para manipulación y visualización de datos
- **ggplot2** — Visualización de datos
- **ggcorrplot** — Visualización de matrices de correlación
- **gridExtra** — Combinación de múltiples gráficos
- **cowplot** — Composición de gráficos
- **scales** — Formateo de escalas y porcentajes
- **kableExtra** — Tablas profesionales
- **plotly** — Gráficos interactivos
- **nortest** — Pruebas de normalidad
- **DT** — Tablas interactivas
- **knitr** — Generación de reportes dinámicos

---

## Autor

**Santiago Jiménez Urrea**
- GitHub: [@sjimenezurrea-sudo](https://github.com/sjimenezurrea-sudo)

