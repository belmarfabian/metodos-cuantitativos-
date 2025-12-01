# Métodos Cuantitativos para Ciencias Sociales

Manual del curso **Métodos Cuantitativos Introductorios** para estudiantes de Ciencia Política de la Universidad Diego Portales, 2025.

**Autor:** Fabián Belmar

---

## 📚 Descripción del Proyecto

Este es un libro digital creado con **bookdown** (R + RMarkdown) que cubre métodos cuantitativos aplicados a ciencias sociales con enfoque en ejemplos chilenos y latinoamericanos.

---

## 🛠️ Requisitos Técnicos

### Software necesario:
1. **R** (versión 4.5.1 o superior)
2. **RStudio** (recomendado)
3. **Pandoc** (incluido con RStudio)

### Paquetes de R requeridos:
```r
install.packages(c(
  'bookdown',
  'knitr',
  'rmarkdown',
  'tidyverse',
  'ggplot2',
  'dplyr',
  'haven',
  'readr',
  'broom'
), repos='https://cran.rstudio.com/')
```

---

## 📂 Estructura del Proyecto

```
metodos_cuantitativos/
├── index.Rmd                    # Prefacio y configuración
├── _output.yml                  # Configuración de salida
├── _bookdown.yml                # Configuración de bookdown
├── book.bib                     # Referencias bibliográficas
├── packages.bib                 # Referencias de paquetes R (generado automáticamente)
├── css/
│   └── style.css                # Estilos personalizados (solo bloques de contenido)
├── images/
│   └── cover.png                # Imagen de portada
├── data/                        # Datos de ejemplo
└── Capítulos:
    ├── 01-introduccion.Rmd
    ├── 02-diseno-investigacion.Rmd
    ├── 03-medicion.Rmd
    ├── 04-datos.Rmd
    ├── 05-estadistica-descriptiva.Rmd
    ├── 06-visualizacion.Rmd
    ├── 07-probabilidad.Rmd
    ├── 08-inferencia.Rmd
    ├── 09-pruebas-hipotesis.Rmd
    ├── 10-comparacion-medias.Rmd
    ├── 11-regresion-bivariada.Rmd
    ├── 12-regresion-multiple.Rmd
    ├── 13-supuestos-ols.Rmd
    ├── 14-glm.Rmd
    └── referencias.Rmd
```

---

## 🚀 Compilación del Libro

### Desde RStudio (recomendado):
1. Abrir el proyecto `metodos_cuantitativos.Rproj`
2. Abrir `index.Rmd`
3. Click en **Build Book** → **bookdown::gitbook**

### Desde R Console:
```r
bookdown::render_book("index.Rmd", "bookdown::gitbook")
```

### Limpiar compilación anterior:
Cerrar el navegador que muestra el libro, luego:
```r
bookdown::clean_book()
```

---

## 📖 Estructura de Contenidos

### Capítulos con contenido completo:
- ✅ **Cap. 1**: Introducción - El método científico en ciencias sociales (~156 líneas)
- ✅ **Cap. 2**: Diseño de investigación (~263 líneas)
- ✅ **Cap. 3**: Medición - De conceptos a variables (~332 líneas)
- ✅ **Cap. 4**: Trabajando con datos (~831 líneas)
- ✅ **Cap. 5**: Estadística descriptiva (~757 líneas)
- ✅ **Cap. 6**: Visualización de datos (~813 líneas)

### Capítulos pendientes:
- ⏳ **Cap. 7**: Introducción a probabilidad
- ⏳ **Cap. 8**: Inferencia estadística
- ⏳ **Cap. 9**: Pruebas de hipótesis
- ⏳ **Cap. 10**: Comparación de medias
- ⏳ **Cap. 11**: Regresión bivariada
- ⏳ **Cap. 12**: Regresión múltiple
- ⏳ **Cap. 13**: Supuestos de OLS
- ⏳ **Cap. 14**: Modelos lineales generalizados

---

## 🎨 Estilos Personalizados

El archivo `css/style.css` contiene **únicamente** estilos para bloques de contenido especiales:

### Bloques disponibles en RMarkdown:

```markdown
::: {.objetivos}
**Objetivos del capítulo:**
- Objetivo 1
- Objetivo 2
:::

::: {.ejemplo}
**Ejemplo:**
Contenido del ejemplo...
:::

::: {.importante}
**Importante:**
Nota destacada...
:::

::: {.nivel data-nivel="introductorio"}
Contenido para el curso MCI
:::

::: {.nivel data-nivel="avanzado"}
Contenido para cursos avanzados
:::

::: {.nivel data-nivel="prerequisito"}
Contenido de repaso
:::
```

**Diseño visual:** Usa el estilo estándar de bookdown GitBook (limpio, probado, sin problemas de layout).

---

## 📝 Sintaxis Especial de RMarkdown

### Footnotes
```markdown
Texto principal^[Contenido de la nota al pie].
```

### Referencias bibliográficas
```markdown
[@autor2020]                  # (Autor, 2020)
@autor2020                    # Autor (2020)
[@autor2020; @otro2021]       # (Autor, 2020; Otro, 2021)
```

### Código R
````markdown
```{r nombre-chunk, echo=TRUE, fig.width=6}
# Código R aquí
plot(1:10)
```
````

---

## 🔧 Solución de Problemas

### No se puede eliminar `_book/`
**Causa:** Archivo `index.html` abierto en navegador
**Solución:** Cerrar navegador, luego `rm -rf _book`

### Cambios en CSS no se reflejan
**Solución:**
1. Cerrar navegador
2. `rm -rf _book`
3. Recompilar
4. Hard refresh (Ctrl+F5)

### Error de compilación
**Solución:**
1. Verificar que todos los paquetes están instalados
2. Cerrar otros procesos de R/RStudio
3. Limpiar cache: `bookdown::clean_book()`

---

## 📦 Migración a Otro Computador

### Archivos esenciales a copiar:
- ✅ Todos los `.Rmd` (contenido)
- ✅ `_output.yml`, `_bookdown.yml`, `index.Rmd`
- ✅ `css/style.css`
- ✅ `book.bib`
- ✅ `images/`, `data/`
- ❌ `_book/`, `*_files/`, `*_cache/` (NO copiar, se regeneran)
- ❌ `packages.bib` (se regenera automáticamente)

### En el nuevo PC:
1. Instalar R y RStudio
2. Instalar paquetes (ver sección "Requisitos Técnicos")
3. Abrir proyecto y compilar

---

## 🎯 Cambios en la Reestructuración (2025-11-16)

### ✅ Limpieza realizada:
- Eliminado todo CSS personalizado que causaba problemas de layout
- Eliminados archivos vacíos `*-part-*.Rmd` (divisores de sección)
- Eliminada carpeta `{data,images,css}` con nombre incorrecto
- Eliminados cache y archivos temporales
- Simplificados archivos de configuración

### ✅ Configuración actual:
- **Diseño:** Bookdown GitBook estándar (sin modificaciones visuales)
- **CSS:** Solo bloques de contenido (`.objetivos`, `.ejemplo`, `.importante`, `.nivel`)
- **TOC:** Comportamiento estándar de bookdown (colapsable por sección)
- **Texto:** Alineación estándar (izquierda)
- **Estructura:** Lineal sin separadores de parte

### 💡 Filosofía de diseño:
- **Contenido > Formato:** Priorizar escritura sobre diseño visual
- **Estándar probado:** Usar configuración por defecto de bookdown
- **Sin personalizaciones complejas:** Evitar CSS que pueda romper el layout
- **Bloques mínimos:** Solo estilos necesarios para el contenido didáctico

---

## 📋 Próximos Pasos

1. **Compilar libro limpio** para verificar que todo funciona
2. **Continuar desarrollando capítulos** 7-14
3. **Agregar datos de ejemplo** en carpeta `data/`
4. **Revisar y expandir** capítulos existentes según sea necesario

---

## 📧 Información

**Autor:** Fabián Belmar
**Institución:** Universidad Diego Portales
**Curso:** Métodos Cuantitativos Introductorios
**Año:** 2025

---

**Última actualización:** 16 de noviembre de 2025
**Versión:** 2.0 - Reestructuración limpia
