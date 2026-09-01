# 7. Plantilla de recogida de datos: la base de datos bien hecha desde el día uno

**[Español](#español) | [English](#english)**

---

## Español

La mitad del sufrimiento estadístico de un proyecto se decide antes de recoger el primer dato: en cómo se diseña la hoja de recogida. Una base bien montada se analiza en horas; una mal montada cuesta semanas de limpieza. Esta plantilla es el encargo que más se repite en mis formaciones, en formato listo para usar.

**Archivo**: [`plantilla_diccionario_variables.md`](plantilla_diccionario_variables.md)

### Las 10 reglas de una base de datos analizable

1. **Una fila por paciente** (o por episodio, si así se define la unidad de análisis; pero solo una unidad).
2. **Una columna por variable**: nunca mezcles dos datos en una celda ("HTA y DM" es una celda inservible; son dos columnas binarias).
3. **Códigos, no texto libre**: sexo como 0/1 con su leyenda en el diccionario, no "mujer", "Mujer", "M" y "fem" conviviendo.
4. **Identificador anonimizado** (P001, P002...) y la tabla de correspondencia con la historia clínica guardada aparte, en un entorno seguro del centro, nunca en la misma hoja ni en la nube.
5. **Fechas en formato ISO** (AAAA-MM-DD) y en columnas de fecha reales, no texto.
6. **Los perdidos, en blanco**: nada de 999, "ND", guiones ni ceros que signifiquen "no consta".
7. **Unidades fijadas de antemano** y anotadas en el diccionario (creatinina en mg/dl o en µmol/l, pero solo una).
8. **Sin formato con significado**: los colores y negritas de Excel no se exportan; si un dato importa, merece su propia columna.
9. **Variables derivadas, aparte**: el IMC se calcula desde peso y talla en el análisis; si lo tecleas a mano, tarde o temprano contradirá a sus padres.
10. **Diccionario de variables desde el primer día**: la pestaña o archivo que explica cada columna. Es la diferencia entre una base y un acertijo.

### Prompt: genera tu hoja de recogida con IA

```
Actúa como metodólogo de investigación clínica. Mi pregunta de
investigación es: [pega tu pregunta PICO]. Mi diseño es [tipo de
estudio] y recogeré datos de [fuente: historia clínica, encuesta...].

Diseña mi hoja de recogida de datos:
1. Propón la lista de variables necesarias (identificación,
   demográficas, exposición, desenlaces, covariables y confusores),
   justificando cada bloque.
2. Para cada variable: nombre corto sin espacios ni tildes, tipo,
   unidades o categorías con sus códigos, y rango plausible.
3. Presenta el resultado como diccionario de variables en tabla,
   siguiendo las reglas de una base analizable (una fila por paciente,
   códigos numéricos, perdidos en blanco, fechas ISO).
4. Señala qué variables suelen dar problemas de calidad en este tipo
   de estudio y cómo prevenirlos en el momento de la recogida.
```

### El paso que casi nadie da

Antes de recoger datos reales, rellena la hoja con 5 pacientes inventados y pásala por el [copiloto de estadística del recurso 6](../06-copiloto-estadistica/README.md). Si la fase de auditoría encuentra problemas con 5 filas ficticias, imagina con 300 reales.

---

## English

Half of a project's statistical suffering is decided before the first data point is collected: in how the collection sheet is designed. A well-built database is analyzed in hours; a badly built one costs weeks of cleaning. This template is the most repeated request in my training programs, in ready-to-use format.

**File**: [`plantilla_diccionario_variables.md`](plantilla_diccionario_variables.md)

### The 10 rules of an analyzable database

One row per patient (one unit of analysis only). One column per variable, never two facts in one cell. Codes, not free text (sex as 0/1 with its legend, not "female", "F" and "fem" coexisting). A de-identified ID (P001...) with the correspondence table stored separately in a secure institutional environment. ISO dates (YYYY-MM-DD). Missing values left blank, never 999 or "N/A". Units fixed in advance and noted in the dictionary. No meaning carried by Excel colors or bold. Derived variables (like BMI) calculated at analysis time, not typed by hand. And a variable dictionary from day one: the tab or file explaining every column.

### Prompt: generate your collection sheet with AI

```
Act as a clinical research methodologist. My research question is:
[paste your PICO question]. My design is [study type] and I will
collect data from [source].

Design my data collection sheet:
1. Propose the list of needed variables (identification, demographics,
   exposure, outcomes, covariates and confounders), justifying each
   block.
2. For each variable: short name without spaces or accents, type,
   units or categories with their codes, and plausible range.
3. Present the result as a variable dictionary table, following the
   rules of an analyzable database (one row per patient, numeric
   codes, blanks for missing, ISO dates).
4. Point out which variables typically cause quality problems in this
   type of study and how to prevent them at collection time.
```

### The step almost nobody takes

Before collecting real data, fill the sheet with 5 invented patients and run it through the [statistics copilot from resource 6](../06-copiloto-estadistica/README.md). If the audit phase finds problems with 5 fictional rows, imagine with 300 real ones.

---

[← Volver al inicio / Back to home](../README.md)
