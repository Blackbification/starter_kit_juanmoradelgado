# 6. Copiloto de estadística clínica: instálalo y analiza con método

**[Español](#español) | [English](#english)**

---

## Español

El error más habitual al analizar datos con IA no es técnico, es de orden: pedir "hazme la estadística" y aceptar lo primero que salga. Este copiloto instala un flujo de trabajo por fases que obliga a hacer las cosas en el orden correcto: primero entender los datos, luego auditarlos y solo después analizar.

### Cómo instalarlo

1. Copia el contenido de [`prompt_copiloto_estadistica_es.md`](prompt_copiloto_estadistica_es.md) (o la [versión en inglés](prompt_copiloto_estadistica_en.md)).
2. Pégalo como instrucciones de un proyecto de Claude o un GPT personalizado (o como primer mensaje de una conversación).
3. Sube tu base de datos **anonimizada** (o la [base sintética del recurso 3](../03-dataset-sintetico/README.md) para practicar) y dile tu pregunta de investigación.
4. El copiloto avanza fase a fase y te pide confirmación antes de pasar a la siguiente.

### Qué hace esta versión lite

Recorre las 6 fases esenciales: encuadre de la pregunta, diccionario de variables, auditoría de calidad del dato, análisis descriptivo con tabla 1, comprobación de supuestos con elección justificada del test, y análisis principal con redacción de resultados.

### Qué NO hace (y la versión completa sí)

La versión completa que trabajamos en mis programas añade el manejo sistemático de valores perdidos e imputación, los modelos multivariables con estrategia de selección de variables, el diagnóstico del modelo, los análisis de sensibilidad y la exportación con sintaxis reproducible para SPSS, R y Python. Más en [juanmoradelgado.com](https://juanmoradelgado.com).

### Regla de oro

La IA propone y calcula; las decisiones metodológicas (variable principal, confusores, manejo de perdidos) son tuyas y deben quedar registradas. La [checklist del recurso 8](../08-checklist-ia-transparente/README.md) te ayuda a dejar constancia.

---

## English

The most common mistake when analyzing data with AI is not technical, it is one of order: asking "do my stats" and accepting whatever comes out. This copilot installs a phased workflow that forces things to happen in the right order: first understand the data, then audit it, and only then analyze.

### How to install it

1. Copy the content of [`prompt_copiloto_estadistica_en.md`](prompt_copiloto_estadistica_en.md) (or the [Spanish version](prompt_copiloto_estadistica_es.md)).
2. Paste it as instructions of a Claude Project or a custom GPT (or as the first message of a conversation).
3. Upload your **de-identified** database (or the [synthetic dataset from resource 3](../03-dataset-sintetico/README.md) to practice) and state your research question.
4. The copilot advances phase by phase and asks for your confirmation before moving on.

### What this lite version does

It walks the 6 essential phases: question framing, variable dictionary, data quality audit, descriptive analysis with Table 1, assumption checking with justified test selection, and the main analysis with results write-up.

### What it does NOT do (and the full version does)

The full version used in my programs adds systematic missing data handling and imputation, multivariable models with a variable selection strategy, model diagnostics, sensitivity analyses and reproducible syntax export for SPSS, R and Python. More at [juanmoradelgado.com](https://juanmoradelgado.com).

---

[← Volver al inicio / Back to home](../README.md)
