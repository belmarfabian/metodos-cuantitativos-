# Notas de Desarrollo - Manual de Métodos Cuantitativos

**Fecha:** 9 de diciembre de 2025
**Proyecto:** Manual de Métodos Cuantitativos para Ciencias Sociales - UDP

---

## Resumen de cambios realizados en esta sesión

### 1. Ejercicios expandidos (Capítulos 9-11)

Los ejercicios de los capítulos finales estaban muy escasos comparados con los anteriores. Se expandieron significativamente:

| Capítulo | Antes | Después |
|----------|-------|---------|
| Cap 9 (Pruebas de hipótesis) | 3 ejercicios breves | 7 ejercicios con secciones conceptuales y aplicadas |
| Cap 10 (Comparación de medias) | 3 ejercicios breves | 7 ejercicios con código R detallado |
| Cap 11 (Regresión bivariada) | 4 ejercicios breves | 8 ejercicios incluyendo caso aplicado |

**Estructura de los nuevos ejercicios:**
- Sección **Conceptuales** para comprensión teórica
- Sección **Aplicados** con código R ejecutable
- Sub-ítems (a, b, c, d) para guiar el análisis

**Archivo modificado:** `anexo-ejercicios.qmd`

### 2. Tablas de resumen estandarizadas (Capítulos 1-3)

Los capítulos 1-3 tenían resúmenes en párrafos de texto, mientras que los capítulos 4-11 usaban tablas. Se convirtieron a formato tabla para consistencia:

- **Cap 1 (Introducción):** Tabla con método científico, cuantificación, teoría, secuencia de investigación + fortalezas/limitaciones
- **Cap 2 (Diseño):** Dos tablas - tipos de preguntas y comparación de diseños (experimental, cuasi-experimental, observacional)
- **Cap 3 (Medición):** Dos tablas - conceptos de medición y niveles de medición (nominal, ordinal, intervalo, razón)

**Archivos modificados:** `01-introduccion.qmd`, `02-diseno-investigacion.qmd`, `03-medicion.qmd`

### 3. Corrección de CSS

Se modificó el archivo `css/style.css` para quitar `text-transform: uppercase` de los bloques `.nivel::before`. Esto afecta cómo se muestra la etiqueta "Métodos Cuantitativos Avanzados" en los bloques de contenido avanzado.

**Cambio realizado:**
```css
/* Antes */
.nivel::before {
  font-weight: bold;
  text-transform: uppercase;  /* ELIMINADO */
  font-size: 0.85em;
  display: block;
  margin-bottom: 10px;
}

/* Después */
.nivel::before {
  font-weight: bold;
  font-size: 0.85em;
  display: block;
  margin-bottom: 10px;
  letter-spacing: 0.5px;
}
```

---

## Problema pendiente: Etiqueta "MÉTODOS CUANTITATIVOS AVANZADOS"

En la captura de pantalla se observó que la etiqueta "MÉTODOS CUANTITATIVOS AVANZADOS" aparece en el sidebar izquierdo como un elemento de navegación separado.

**Causa:** El CSS genera esta etiqueta mediante `::before` con `content: "🎓 Métodos Cuantitativos Avanzados"`. El `text-transform: uppercase` ya fue removido.

**Opciones para resolver (pendiente de decisión del usuario):**
1. Mantener la etiqueta pero en minúsculas (ya implementado)
2. Eliminar la etiqueta completamente (el contenido avanzado no tendría marcador visual)
3. Usar un formato diferente (ej: solo el emoji 🎓, o texto más corto como "Avanzado")

Para implementar opción 2 o 3, modificar en `css/style.css`:
```css
.nivel[data-nivel="avanzado"]::before {
  content: "🎓 Avanzado";  /* Opción 3: texto corto */
  /* O content: "";  para opción 2: sin etiqueta */
  color: #7c3aed;
}
```

---

## Estructura actual del libro

### Capítulos incluidos en `_quarto.yml`:
1. index.qmd (Prefacio)
2. 01-introduccion.qmd
3. 02-diseno-investigacion.qmd
4. 03-medicion.qmd
5. 04-datos.qmd
6. 05-estadistica-descriptiva.qmd
7. 06-visualizacion.qmd
8. 07-probabilidad.qmd
9. 08-inferencia.qmd
10. 09-pruebas-hipotesis.qmd
11. 10-comparacion-medias.qmd
12. 11-regresion-bivariada.qmd
13. anexo-ejercicios.qmd

### Archivos NO incluidos (esqueletos vacíos):
- 12-regresion-multiple.qmd
- 13-supuestos-ols.qmd
- 14-glm.qmd
- referencias.qmd

---

## Estructura consistente de cada capítulo

Todos los capítulos ahora siguen esta estructura:
1. **Título y etiqueta** (`# Título {#etiqueta}`)
2. **Setup chunk** (caps 4-11 tienen `{r setup-XX, include=FALSE}`)
3. **Objetivos del capítulo** (`## Objetivos del capítulo {.unnumbered}`)
4. **Contenido principal** con secciones
5. **Resumen** (`## Resumen {.unnumbered}`) - en formato tabla
6. **Lecturas recomendadas** (`## Lecturas recomendadas {.unnumbered}`)
7. **Ejercicios** (`## Ejercicios {.unnumbered}`) - referencia al anexo
8. **Referencias** (`::: {#refs} :::`)

---

## Notas al pie

Todas las notas al pie están correctamente referenciadas. Formato usado:
- Referencia en texto: `[^nombre-nota]`
- Definición: `[^nombre-nota]: Contenido de la nota...`

Se corrigieron notas huérfanas en sesiones anteriores (caps 05, 09).

---

## Comandos útiles

### Renderizar el libro completo:
```bash
cd "g:/My Drive/Manual cuanti/metodos_cuantitativos"
"/c/Users/fabia/AppData/Local/Programs/Quarto/bin/quarto.exe" render
```

### Renderizar un capítulo específico:
```bash
"/c/Users/fabia/AppData/Local/Programs/Quarto/bin/quarto.exe" render 01-introduccion.qmd
```

### Verificar warnings en el render:
```bash
"/c/Users/fabia/AppData/Local/Programs/Quarto/bin/quarto.exe" render 2>&1 | grep -iE "(warning|error|orphan)"
```

---

## Estado del libro

- **Renderizado:** Sin errores
- **Warnings:** Solo uno menor de ggrepel (overlaps en gráfico)
- **Notas al pie:** Todas correctamente vinculadas
- **Estructura:** Consistente en todos los capítulos
- **Ejercicios:** Completos y detallados para todos los capítulos

---

## Próximos pasos sugeridos

1. Decidir qué hacer con la etiqueta "Métodos Cuantitativos Avanzados" en el CSS
2. Considerar agregar setup chunks a caps 1-3 si se desea consistencia total
3. Desarrollar capítulos 12-14 cuando sea necesario
4. Revisar que las referencias bibliográficas (@citas) estén todas en book.bib
