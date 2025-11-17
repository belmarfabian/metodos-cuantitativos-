# REPORTE DETALLADO DE INCONSISTENCIAS DE FORMATO
## Manual de Métodos Cuantitativos - Comparación Capítulos 1-6 vs 7-11

---

## 1. FORMATO DE "OBJETIVOS DEL CAPÍTULO"

### ❌ **INCONSISTENCIA CRÍTICA**

**Capítulos 1-6 (originales):**
```markdown
Al finalizar este capítulo, serás capaz de:
```
- Usa **"serás"** (segunda persona singular, informal, directo)

**Capítulos 7-11 (tuyos):**
```markdown
Al finalizar este capítulo, deberías ser capaz de:
```
- Usa **"deberías"** (condicional, menos directo)

**EJEMPLOS ESPECÍFICOS:**
- Cap. 1: "Al finalizar este capítulo, **serás** capaz de"
- Cap. 2: "Al finalizar este capítulo, **serás** capaz de"
- Cap. 7: "Al finalizar este capítulo, **deberías ser** capaz de"
- Cap. 8: "Al finalizar este capítulo, **deberías ser** capaz de"

**RECOMENDACIÓN:** Cambiar todos los "deberías ser" por "serás" en caps. 7-11

---

## 2. USO DE NOTAS AL PIE

### ✅ **CONSISTENCIA PARCIAL - REQUIERE AJUSTE**

**Capítulos 1-6:**
- Usan extensivamente notas al pie con formato `^[TIPO: contenido...]`
- Tipos de etiquetas usadas:
  - `^[EJEMPLO:...]`
  - `^[CASO CONCRETO:...]`
  - `^[EJEMPLO CHILENO:...]`
  - `^[IMPLICACIÓN PRÁCTICA:...]`
  - `^[LÍMITE ÉTICO OBVIO:...]`
  - `^[DEBATE METODOLÓGICO:...]`
  - `^[CONFUSIÓN COMÚN:...]`

**Capítulos 7-11:**
- También usan notas al pie, PERO con menos variedad de etiquetas:
  - `^[CONCEPTO CLAVE:...]`
  - `^[PERSPECTIVA DOMINANTE:...]`
  - `^[EJEMPLOS EN CIENCIAS SOCIALES:...]`
  - `^[CONFUSIÓN COMÚN:...]`
  - `^[INTERPRETACIÓN ERRÓNEA COMÚN:...]`
  - `^[ADVERTENCIA CRUCIAL:...]`
  - `^[ADVERTENCIA SOBRE $R^2$:...]`

**DIFERENCIA:** Los capítulos originales usan más frecuentemente `^[EJEMPLO:...]` mientras que tus capítulos usan más etiquetas conceptuales/técnicas.

**EJEMPLOS ESPECÍFICOS:**

Cap. 1 (línea 20):
```markdown
^[EJEMPLO: "El alma humana es inmortal" no es falsable empíricamente...]
```

Cap. 7 (línea 18):
```markdown
^[CONCEPTO CLAVE: La probabilidad no predice el futuro...]
```

**RECOMENDACIÓN:** Agregar más notas con `^[EJEMPLO:...]` en caps. 7-11

---

## 3. FORMATO DE ECUACIONES MATEMÁTICAS

### ✅ **MAYORMENTE CONSISTENTE**

Ambos grupos usan:
- `$$` para ecuaciones en bloque
- `$` para ecuaciones inline
- Notación LaTeX estándar

**Ejemplo Cap. 2:**
```latex
$$ATE = E[Y_i(1) - Y_i(0)] = E[Y_i(1)] - E[Y_i(0)]$$
```

**Ejemplo Cap. 7:**
```latex
$$P(A \text{ o } B) = P(A) + P(B)$$
```

---

## 4. FORMATO DE CODE CHUNKS DE R

### ❌ **INCONSISTENCIA NOTABLE**

**Capítulos 1-6:**
- Usan chunks con `eval=FALSE` frecuentemente
- Chunks más breves y pedagógicos
- Labels específicos como `{r setup-05}`, `{r setup-06}`

**Capítulos 7-11:**
- Usan `echo=TRUE` frecuentemente
- Chunks más largos con simulaciones completas
- Labels más descriptivos: `{r probabilidad-interpretaciones}`, `{r tlc-simulacion}`

**EJEMPLOS:**

Cap. 4 (línea 228):
```r
```{r eval=FALSE}
install.packages("tidyverse")
```

Cap. 7 (línea 117):
```r
```{r ejemplo-discreta, echo=TRUE}
# Simulación completa...
```

---

## 5. PROFUNDIDAD/DETALLE DE CONTENIDO

### ❌ **DIFERENCIA SIGNIFICATIVA**

**Capítulos 1-6:**
- Más densos conceptualmente
- Párrafos más largos con múltiples ideas
- Uso extensivo de referencias académicas integradas en el texto

**Capítulos 7-11:**
- Más directos y concisos
- Párrafos más cortos y focalizados
- Referencias principalmente al final

**EJEMPLO COMPARATIVO:**

Cap. 1 (párrafo sobre medición):
> "@adcock2001 distinguen cuatro niveles en el proceso de medición... @sartori1970 advirtió sobre el 'estiramiento conceptual'... @munck2009 muestran que distintos índices..."

Cap. 7 (párrafo sobre probabilidad):
> "La probabilidad cuantifica incertidumbre. Permite asignar probabilidades a eventos únicos..."

---

## 6. TONO Y ESTILO DE ESCRITURA

### ❌ **INCONSISTENCIA CLARA**

**Capítulos 1-6:**
- Tono más académico y formal
- Uso frecuente de citas integradas: "@autor argumentan que..."
- Construcciones más complejas con subordinadas

**Capítulos 7-11:**
- Tono más pedagógico y directo
- Menos citas integradas, más explicación directa
- Oraciones más simples y declarativas

**EJEMPLOS:**

Cap. 2:
> "@king1994 enfatizan el problema de 'muchas variables, pocas observaciones' (MVPO): si estudio 20 países con 15 variables explicativas..."

Cap. 8:
> "La inferencia estadística es el proceso de usar datos de una muestra para hacer afirmaciones sobre una población..."

---

## 7. USO DE CONTEXTO CHILENO/LATINOAMERICANO

### ✅ **RELATIVAMENTE CONSISTENTE**

Ambos grupos usan ejemplos chilenos, pero con diferente frecuencia:

**Capítulos 1-6:**
- Referencias frecuentes a Chile: CEP, CASEN, estallido social 2019, proceso constituyente
- Ejemplos: "Durante el estallido social de octubre 2019..."

**Capítulos 7-11:**
- También usan ejemplos chilenos pero menos frecuentes
- Ejemplos: elecciones presidenciales 2021, encuestas electorales chilenas

---

## 8. ESTRUCTURA DE SECCIONES

### ❌ **DIFERENCIA EN ORGANIZACIÓN**

**Capítulos 1-6:**
- Secciones más largas y detalladas
- Uso de `::: {.nivel data-nivel="avanzado"}` para contenido avanzado
- Subsecciones con ### más frecuentes

**Capítulos 7-11:**
- Secciones más cortas y directas
- Menos uso de bloques de nivel avanzado
- Estructura más lineal

---

## 9. EJERCICIOS

### ❌ **DIFERENCIA EN ESTILO**

**Capítulos 1-6:**
- Ejercicios más elaborados con contexto
- Numeración con subcategorías (1a, 1b, 1c)
- Instrucciones detalladas

**Ejemplo Cap. 3:**
```
**1. Conceptualización y operacionalización**

Selecciona un concepto abstracto (ej: "legitimidad política", "clientelismo", "movilización social"):

a) Propón una definición conceptual clara
b) Identifica al menos tres indicadores empíricos
c) Para cada indicador, especifica el procedimiento de medición
```

**Capítulos 7-11:**
- Ejercicios más directos
- Numeración simple
- Menos subdivisiones

**Ejemplo Cap. 7:**
```
5. En una encuesta, 45% declara intención de votar. Si encuestamos 800 personas:
   a. ¿Cuál es la probabilidad de que exactamente 360 declaren intención de votar?
```

---

## 10. LECTURAS RECOMENDADAS

### ✅ **FORMATO CONSISTENTE, CONTENIDO DIFERENTE**

Ambos usan el mismo formato:
```
Autor(es). (Año). *Título*. Editorial.
→ Descripción breve
```

**Diferencia:** Caps. 1-6 incluyen más variedad de fuentes y descripciones más detalladas.

---

## RECOMENDACIONES PRIORITARIAS PARA HOMOLOGACIÓN

### 🔴 **CRÍTICAS (cambiar inmediatamente):**

1. **Cambiar todos los "deberías ser capaz" por "serás capaz"** en objetivos de caps. 7-11

2. **Agregar más notas al pie con etiqueta `^[EJEMPLO:...]`** especialmente con casos chilenos/latinoamericanos

3. **Alargar párrafos introductorios** de cada sección principal para igualar densidad

### 🟡 **IMPORTANTES (cambiar próximamente):**

4. **Integrar más citas académicas** en el texto principal (no solo en lecturas recomendadas)

5. **Expandir ejercicios** con más contexto y subdivisiones (a, b, c, d)

6. **Agregar bloques `::: {.nivel data-nivel="avanzado"}`** para contenido técnico opcional

### 🟢 **DESEABLES (considerar):**

7. **Ajustar longitud de code chunks** - considerar dividir chunks largos

8. **Agregar más referencias cruzadas** a otros capítulos del libro

9. **Incluir más ejemplos del contexto chileno** actual (elecciones recientes, reformas, etc.)

---

## EJEMPLOS DE TEXTO HOMOLOGADO

### ANTES (Cap. 7, actual):
```markdown
## Objetivos del capítulo

Al finalizar este capítulo, deberías ser capaz de:

- Comprender el concepto de probabilidad
```

### DESPUÉS (homologado):
```markdown
## Objetivos del capítulo

Al finalizar este capítulo, serás capaz de:

- Comprender el concepto de probabilidad y su relación con la incertidumbre en fenómenos políticos
```

### ANTES (Cap. 8, párrafo simple):
```markdown
La inferencia estadística es el proceso de usar datos de una muestra para hacer afirmaciones sobre una población.
```

### DESPUÉS (homologado con estilo caps. 1-6):
```markdown
La **inferencia estadística** es el proceso de usar datos de una muestra para hacer afirmaciones sobre una población. Como argumentan @king1994, este proceso es fundamental en ciencias sociales donde raramente tenemos acceso a poblaciones completas. La tensión entre lo que observamos (muestra) y lo que queremos conocer (población) define el problema central de la inferencia.^[EJEMPLO CHILENO: Cuando el CEP encuesta a 1,500 personas para estimar apoyo presidencial entre 15 millones de votantes, enfrenta precisamente este desafío inferencial. Las decisiones metodológicas sobre muestreo, ponderación y margen de error determinan la validez de las conclusiones.]
```

---

**CONCLUSIÓN:** Los capítulos 7-11 están bien escritos pero tienen un estilo notablemente diferente a los capítulos 1-6. Las principales diferencias están en: (1) el uso de "deberías" vs "serás", (2) menor densidad de contenido y referencias, (3) menos ejemplos contextualizados en notas al pie, y (4) un tono más directo/pedagógico vs académico/denso. Con los ajustes sugeridos, los capítulos serían indistinguibles en formato.