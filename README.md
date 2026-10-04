
# EDA: Tiempo en Pantallas, Sueño y Salud Mental en Adolescentes

Análisis Exploratorio de Datos (EDA) sobre cómo el tiempo frente a pantallas y los patrones de sueño afectan la salud mental de los adolescentes. Este proyecto está desarrollado en **R** y **R Markdown** con formato **Bookdown**.

---

## Dataset

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

## ⚙️ Requisitos

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
