# Resumen de Sesión de Trabajo - 4 de Diciembre 2024

## Cambios Realizados en Esta Sesión

### 1. Contenido marcado como "Avanzado"

Se agregaron bloques `::: {.nivel data-nivel="avanzado"}` en los siguientes capítulos para indicar contenido opcional que va más allá del examen:

**Capítulo 02 (Diseño de investigación):**
- Efectos fijos en datos de panel
- Técnicas avanzadas de inferencia causal (matching, diseños cuasi-experimentales, análisis de sensibilidad)
- Falacias de nivel de análisis (ecológica/atómica)
- Problema de "muchas variables, pocas observaciones"

**Capítulo 04 (Datos) - REDUCIDO:**
- Catálogo completo de fuentes de datos
- Datos en línea y bases de datos SQL
- Agregar datos por grupos (group_by/summarise)
- Unir datasets (joins)
- R Markdown y Quarto

**Capítulo 07 (Probabilidad):**
- Interpretación bayesiana de probabilidad
- Fórmulas matemáticas con integrales

**Capítulo 08 (Inferencia):**
- Determinación del tamaño muestral (fórmulas y tabla)

**Capítulo 09 (Pruebas de hipótesis):**
- d de Cohen y tamaño del efecto estandarizado
- Problema de comparaciones múltiples y corrección de Bonferroni

---

### 2. Actualización del Prefacio (index.qmd)

Se agregó al inicio:

```markdown
## Objetivo de este manual {.unnumbered}

Este es un **manual de preparación para el examen** del curso Métodos Cuantitativos Introductorios. Su propósito es presentar de forma clara y concisa los conceptos fundamentales que necesitas dominar para aprobar el curso.

::: {.callout-note}
## Contenido avanzado
Las secciones marcadas como **"Avanzado"** contienen material complementario que va más allá de lo requerido para el examen. Puedes omitirlas en tu primera lectura y volver a ellas si deseas profundizar.
:::
```

---

### 3. Configuración de bibliografía por capítulo

**Archivo:** `_quarto.yml`

```yaml
format:
  html:
    citations-hover: true
    citeproc: true
    split-bibliography: true  # Cada capítulo tiene su propia bibliografía
```

**Archivo:** `css/style.css`

```css
#refs {
  display: block !important;  /* Fuerza mostrar referencias */
  max-width: 800px;
  margin-left: auto;
  margin-right: auto;
  margin-top: 2em;
  padding-top: 1em;
  border-top: 1px solid #e0e0e0;
}
```

**Resultado:**
- Notas al pie aparecen al margen (estilo Tufte)
- Bibliografía citada aparece al final de cada capítulo

---

## Estructura del Proyecto

```
metodos_cuantitativos/
├── _quarto.yml              # Configuración principal
├── css/style.css            # Estilos personalizados
├── book.bib                 # Bibliografía
├── apa.csl                  # Formato de citas APA
├── index.qmd                # Portada (actualizada)
├── 01-introduccion.qmd
├── 02-diseno-investigacion.qmd  # Con bloques avanzados
├── 03-medicion.qmd
├── 04-datos.qmd             # Reducido con bloques avanzados
├── 05-estadistica-descriptiva.qmd
├── 06-visualizacion.qmd
├── 07-probabilidad.qmd      # Con bloques avanzados
├── 08-inferencia.qmd        # Con bloques avanzados
├── 09-pruebas-hipotesis.qmd # Con bloques avanzados
├── 10-comparacion-medias.qmd
├── 11-regresion-bivariada.qmd
├── anexo-ejercicios.qmd
└── docs/                    # Output HTML generado
```

---

## Comandos útiles

**Renderizar todo el libro:**
```bash
"/c/Users/fabia/AppData/Local/Programs/Quarto/bin/quarto.exe" render "g:/My Drive/Manual cuanti/metodos_cuantitativos"
```

**Renderizar un solo capítulo:**
```bash
"/c/Users/fabia/AppData/Local/Programs/Quarto/bin/quarto.exe" render "g:/My Drive/Manual cuanti/metodos_cuantitativos/index.qmd"
```

---

## Git - Commits realizados

1. `48f9a6b` - Marcar contenido avanzado y configurar bibliografía por capítulo
2. `1665770` - Agregar objetivo del manual en prefacio

**Repositorio:** https://github.com/belmarfabian/metodos-cuantitativos-.git

---

## Tareas Pendientes (si las hay)

- Revisar warning de `:::` suelto en 04-datos.qmd (cosmético, no afecta compilación)
- Verificar visualmente los bloques "avanzado" en el HTML renderizado

---

## Notas Importantes

1. **Bloques avanzados:** Usan la clase `.nivel[data-nivel="avanzado"]` que ya tiene estilos en `css/style.css`

2. **Bibliografía:** Cada capítulo debe terminar con:
```markdown
::: {#refs}
:::
```

3. **El libro compila correctamente** - Último render exitoso
