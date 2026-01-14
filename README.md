# Métodos Cuantitativos para Ciencias Sociales

Manual del curso **Métodos Cuantitativos Introductorios** para estudiantes de Ciencia Política de la Universidad Diego Portales, 2025.

**Autor:** Fabián Belmar

---

## Descripción

Libro digital creado con **Quarto** que cubre métodos cuantitativos aplicados a ciencias sociales, con enfoque en ejemplos chilenos y latinoamericanos.

---

## Estructura del Libro

| Parte | Contenido |
|-------|-----------|
| I. Prerequisitos | Introducción, Diseño de investigación |
| II. Generalidades | Medición, Trabajo con datos |
| III. Estadística Descriptiva | Estadística descriptiva, Visualización |
| IV. Inferencia Estadística | Probabilidad, Inferencia, Pruebas de hipótesis |
| V. Análisis Bivariado | Comparación de medias, Regresión bivariada |
| Anexos | Ejercicios |

---

## Requisitos

- [Quarto](https://quarto.org/) (versión 1.3 o superior)
- [R](https://cran.r-project.org/) (versión 4.0 o superior)
- [RStudio](https://posit.co/download/rstudio-desktop/) (recomendado)

### Paquetes de R

```r
install.packages(c(
  'tidyverse',
  'ggplot2',
  'dplyr',
  'haven',
  'readr',
  'broom',
  'knitr'
))
```

---

## Compilación

### Desde terminal:

```bash
quarto render
```

### Desde RStudio:

1. Abrir el proyecto
2. En la pestaña **Build**, click en **Render Book**

El libro se genera en la carpeta `docs/`.

---

## Estructura del Proyecto

```
metodos-cuantitativos-/
├── _quarto.yml          # Configuración del libro
├── index.qmd            # Portada
├── 01-introduccion.qmd
├── 02-diseno-investigacion.qmd
├── ...
├── anexo-ejercicios.qmd
├── book.bib             # Referencias bibliográficas
├── css/style.css        # Estilos personalizados
└── docs/                # Libro compilado (output)
```

---

## Información

**Autor:** Fabián Belmar  
**Institución:** Universidad Diego Portales  
**Curso:** Métodos Cuantitativos Introductorios  
**Año:** 2025

---

**Última actualización:** Enero 2026
